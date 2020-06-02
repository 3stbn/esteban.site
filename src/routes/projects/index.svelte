<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`projects.json`)
      .then(r => r.json())
      .then(posts => {
        return { posts };
      });
  }
</script>

<script>
  export let posts;
  import Hero from "../../components/Hero.svelte";
  import PostsList from "../../components/PostsList.svelte";
</script>

<svelte:head>
  <title>Blog</title>
</svelte:head>
<div class="container">
  <Hero page="projects" />
  <PostsList {posts} title="Recent Projects" path="projects" />

</div>
