<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";

  export let segment;
</script>

<style>
  main {
    padding-bottom: 3rem;
    flex: 1;
  }
  .site {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
  }
</style>

<svelte:head>
  <style src="../scss/index.scss">

  </style>
  <style src="../scss/variables.scss">

  </style>
</svelte:head>

<div class="site">
  <Nav {segment} />

  <main>
    <slot />
  </main>

  <Footer />

</div>
