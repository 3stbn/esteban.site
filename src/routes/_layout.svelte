<script>
  import Nav from "../components/Nav.svelte";

  export let segment;
</script>

<style>
  main {
    padding-bottom: 3rem;
  }
</style>

<svelte:head>
  <style src="../scss/index.scss">

  </style>
  <style src="../scss/variables.scss">

  </style>
</svelte:head>

<Nav {segment} />

<main>
  <slot />
</main>
