<script>
  export let cover = "";
  export let title = "";
  export let description = "";
  export let tags = [];
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
          <img src={cover} alt="Image" />
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
      {#if tags.length > 0}
        <nav class="level is-mobile">
          <div class="level-left">
            <a class="level-item" aria-label="reply">
              <span class="icon is-small">
                <i class="fas fa-reply" aria-hidden="true" />
              </span>
            </a>
            <a class="level-item" aria-label="retweet">
              <span class="icon is-small">
                <i class="fas fa-retweet" aria-hidden="true" />
              </span>
            </a>
            <a class="level-item" aria-label="like">
              <span class="icon is-small">
                <i class="fas fa-heart" aria-hidden="true" />
              </span>
            </a>
          </div>
        </nav>
      {/if}
    </div>
  </article>
</div>
