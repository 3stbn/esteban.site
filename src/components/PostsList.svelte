<script>
  export let posts = [];
  export let aligment = "left";
</script>

<style type="text/scss">
  @import "../scss/variables.sass";
  .post-list-item {
    border-bottom: 1px solid $purple;
    padding: 0 1rem;
  }

  .posts-list {
    margin-top: 1.75rem;
  }
  .post-list-item h3 {
    display: flex;
    align-items: center;
  }
  .post-tag {
    padding: 0.4rem 0.75rem;
    margin: 0 0.5rem;
  }

  svg line {
    stroke: $purple;
    stroke-width: 1;
  }
</style>

<div class="columns">
  <div class="column is-narrow is-hidden-mobile ">
    <svg width="40" height="170">
      <line x1="20" y1="20" x2="20" y2="170" />
    </svg>
  </div>
  <div class="column posts-list">
    {#each posts as post}
      <div class="post-list-item columns">
        <h3 class="column is-size-5">{post.title}</h3>
        <div class="column has-text-right">
          {#each post.tags as tag}
            <span class="post-tag has-background-link has-text-white">
              {tag}
            </span>
          {/each}
        </div>

      </div>
    {/each}
  </div>
</div>
