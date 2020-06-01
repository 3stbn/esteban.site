<script>
  import LogoSvg from "./svg/LogoSvg.svelte";
  export let segment;
  let isActive = false;
</script>

<style type="text/scss">
  @import "../scss/variables.sass";
  .navbar {
    border-bottom: 1px solid $purple;
    max-height: 100px;
  }
</style>

<nav class="navbar" role="navigation" aria-label="main navigation">
  <div class="container">
    <div class="navbar-brand">
      <a class="navbar-item" href=".">
        <LogoSvg />
        <h1 class="is-size-4 has-text-primary">ESTEBAN.SITE</h1>
      </a>
      <span
        role="button"
        class="navbar-burger burger"
        on:click={() => (isActive = !isActive)}
        class:is-active={isActive}
        aria-label="menu"
        aria-expanded="false"
        data-target="navbarBasicExample">
        <span aria-hidden="true" />
        <span aria-hidden="true" />
        <span aria-hidden="true" />
      </span>
    </div>

    <div class="navbar-menu" class:is-active={isActive}>

      <div class="navbar-end is-size-5">
        <a
          class="navbar-item has-text-primary has-text-weight-light"
          href="projects">
          PROJECTS
        </a>
        <a
          class="navbar-item has-text-primary has-text-weight-light"
          href="blog">
          BLOG
        </a>
      </div>
    </div>
  </div>

</nav>
