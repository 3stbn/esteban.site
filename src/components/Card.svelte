<script>
  export let cover = "";
  export let title = "";
  export let description = "";
</script>

<style>
  .card-blog {
    padding: 2rem;
    box-shadow: -22px 20px 0px 0px rgba(173, 168, 255, 1);
    border: 1px solid #a8a8a8;
    margin: 0 1rem;
  }
</style>

<div class="card-blog">
  <article class="media">
    {#if cover}
      <div class="media-left">
        <figure class="image is-128x128">
          <img src={cover} alt={title} />
        </figure>
      </div>
    {/if}

    <div class="media-content">
      <div class="content">
        <p>
          {#if title}
            <strong>John Smith</strong>
            <br />
          {/if}
          {#if description}
            <span>{description}</span>
            <br />
          {/if}

        </p>
      </div>
    </div>
  </article>
</div>
