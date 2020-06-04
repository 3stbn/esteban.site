<style type="text/scss">
  @import "../scss/variables.sass";
  .social-links {
    margin-top: 3rem;
  }
  .social-link {
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .username {
    margin-left: 1.5rem;
  }
  .copy {
    border-top: 1px solid $purple;
    margin-top: 2rem;
    padding: 1rem;
  }
  footer {
    justify-self: flex-end;
  }
</style>

<footer>
  <div class="container">
    <div class="columns social-links has-text-link">
      <a class="column social-link " href="https://github.com/3stbn">
        <span class="icon is-size-1">
          <i class="fab fa-github" />
        </span>
        <span class=" username">@3stn</span>
      </a>
      <a class="column social-link" href="https://twitter.com/stbantorres">
        <span class="icon is-size-1">
          <i class="fab fa-twitter" />
        </span>
        <span class=" username">@stbantorres</span>
      </a>
      <a
        class="column social-link"
        href="https://www.youtube.com/channel/UCbWV65OoGP6mw2pGd0c5E-g">
        <span class="icon is-size-1">
          <i class="fab fa-youtube" />
        </span>
        <span class=" username">Esteban Codes</span>
      </a>
      <a class="column social-link" href="mailto:hi@esteban.site">
        <span class="icon is-size-1">
          <i class="fas fa-envelope" />
        </span>
        <span class=" username">hi@esteban.site</span>
      </a>
    </div>
  </div>
  <div class="copy">
    <div class="container has-text-centered has-text-link">
      ©{new Date().getFullYear()} Esteban Torres, all rights reserved. Made with
      ❤️ with
      <a href="https://sapper.svelte.dev/">Sapper</a>
    </div>
  </div>
</footer>
