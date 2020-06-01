<script>
  import HomeSvg from "./svg/HomeSvg.svelte";
  import BlogSvg from "./svg/BlogSvg.svelte";
  import ProjectsSvg from "./svg/ProjectsSvg.svelte";
  export let page = "home";
  export let description = "";
</script>

<style>
  .hero-blog {
    margin: 1.5rem 0;
    min-height: calc(100vh - 100px);
  }
  .featured {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
</style>

<div class="columns hero-blog">
  <div class="column has-text-centered featured">
    {#if page === 'home'}
      <HomeSvg />
    {:else if page === 'projects'}
      <ProjectsSvg />
    {:else if page === 'blog'}
      <BlogSvg />
    {/if}
  </div>
  <div class="column featured">
    <h1
      class="has-text-primary is-capitalized has-text-weight-light is-size-1
      has-text-centered">
      {page}
    </h1>
    <p class="is-size-4">{description}</p>
  </div>
</div>
