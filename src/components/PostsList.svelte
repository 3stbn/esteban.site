<script>
  import PostListItem from "./PostListItem.svelte";
  export let title = "";
  export let posts = [];
  export let aligment = "left";
  export let showDate = true;
  export let path;
</script>

<style type="text/scss">
  @import "../scss/variables.sass";

  .posts-list {
    margin-top: 1.75rem;
    cursor: pointer;
  }

  svg line {
    stroke: $purple;
    stroke-width: 1;
  }
  section {
    margin: 0 1rem;
    margin-top: 3rem;
  }
</style>

<section>
  <h2
    class="has-text-primary is-size-4"
    class:has-text-right={aligment === 'right'}>
    {title}
  </h2>
  <br />
  <div class="columns">
    {#if aligment === 'left'}
      <div class="column is-narrow is-hidden-mobile ">
        <svg width="40" height="170">
          <line x1="20" y1="20" x2="20" y2="170" />
        </svg>
      </div>
    {/if}
    <div class="column posts-list">
      {#each posts as post}
        <PostListItem {path} {post} {aligment} {showDate} />
      {/each}
    </div>
    {#if aligment === 'right'}
      <div class="column is-narrow is-hidden-mobile ">
        <svg width="40" height="170">
          <line x1="20" y1="20" x2="20" y2="170" />
        </svg>
      </div>
    {/if}
  </div>

</section>
