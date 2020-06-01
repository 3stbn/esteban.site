<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`blog.json`)
      .then(r => r.json())
      .then(posts => {
        return { posts: posts.slice(0, 3) };
      });
  }
</script>

<script>
  import Hero from "../components/Hero.svelte";
  import Card from "../components/Card.svelte";
  import PostsList from "../components/PostsList.svelte";
  export let posts;
</script>

<svelte:head>
  <title>Esteban</title>
</svelte:head>
<div class="container">

  <Hero page="home" description="Welcome to my personal space" />
  <Card
    description=" Hy my name is Esteban. I work as a developer (I learned it
    after I graduated from marketing). I like music (I listen and also compose
    ). Sometimes I drink coffee even tho I don't really like it" />
  <hr />
  <h2 class="has-text-primary is-size-4 ">Recent Projects</h2>
  <br />
  <PostsList {posts} />
  <h2 class="has-text-primary has-text-right is-size-4 ">Recent Posts</h2>
  <br />
  <PostsList {posts} />

</div>
