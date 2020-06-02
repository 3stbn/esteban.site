<script context="module">
  export async function preload({ params, query }) {
    const postsResult = await this.fetch("blog.json");
    const projectsResult = await this.fetch("projects.json");
    const posts = await postsResult.json();
    const projects = await projectsResult.json();
    return {
      posts: posts
        .sort((a, b) => new Date(b.date).getTime() - new Date(a.date).getTime())
        .slice(0, 3),
      projects: projects
        .sort((a, b) => new Date(b.date).getTime() - new Date(a.date).getTime())
        .slice(0, 3)
    };
  }
</script>

<script>
  import Hero from "../components/Hero.svelte";
  import Card from "../components/Card.svelte";
  import PostsList from "../components/PostsList.svelte";
  export let posts;
  export let projects;
</script>

<svelte:head>
  <title>Esteban</title>
</svelte:head>

<div class="container">

  <Hero page="home" description="Welcome to my personal space" fullHeight>
    <Card
      description=" Hy my name is Esteban. I work as a developer (I learned it
      after I graduated from marketing). I like music (I listen and also compose
      ). Sometimes I drink coffee even tho I don't really like it" />
  </Hero>

  <PostsList
    posts={projects}
    path="projects"
    showDate={false}
    title="Recent Projects" />
  <br />
  <PostsList {posts} path="blog" title="Recent Blog Posts" />
</div>
