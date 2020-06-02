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
      <div class="column social-link ">
        <span class="icon is-size-1">
          <i class="fab fa-github" />
        </span>
        <span class=" username">@3stn</span>
      </div>
      <div class="column social-link">
        <span class="icon is-size-1">
          <i class="fab fa-twitter" />
        </span>
        <span class=" username">@stbantorres</span>
      </div>
      <div class="column social-link">
        <span class="icon is-size-1">
          <i class="fab fa-youtube" />
        </span>
        <span class=" username">Esteban Codes</span>
      </div>
      <div class="column social-link">
        <span class="icon is-size-1">
          <i class="fas fa-envelope" />
        </span>
        <span class=" username">hi@esteban.site</span>
      </div>
    </div>
  </div>
  <div class="copy">
    <div class="container has-text-centered has-text-link">
      ©{new Date().getFullYear()} Esteban Torres, all rights reserved. Made with
      ❤️ with sapper
    </div>
  </div>
</footer>
