<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`blog.json`)
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
  <Hero page="blog" />
  <PostsList {posts} title="Recent Posts" path="blog" />

</div>
