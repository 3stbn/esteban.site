<script>
  export let post = {};
  export let aligment = "left";
  export let showDate = true;
  export let path;
</script>

<style type="text/scss">
  @import "../scss/variables.sass";
  .post-list-item {
    border-bottom: 1px solid $purple;
    padding: 0 1rem;
  }

  .post-tag {
    padding: 0.4rem 0.75rem;
    margin: 0 0.5rem;
  }
</style>

<a class="post-list-item columns" rel="prefetch" href="{path}/{post.slug}">
  {#if aligment === 'left'}
    <h3 class="column is-size-5">{post.title}</h3>
  {/if}
  <div class="column" class:has-text-right={aligment === 'left'}>
    {#if aligment === 'right' && showDate}
      <span>{new Date(post.date).toLocaleDateString()}</span>
    {/if}
    {#each post.tags as tag}
      <span class="post-tag has-background-link has-text-white">{tag}</span>
    {/each}
    {#if aligment === 'left' && showDate}
      <span>{new Date(post.date).toLocaleDateString()}</span>
    {/if}
  </div>
  {#if aligment === 'right'}
    <h3 class="column has-text-right is-size-5">{post.title}</h3>
  {/if}
</a>
