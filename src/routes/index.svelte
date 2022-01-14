<script lang="ts">
  import { isLoading } from '../stores'

  function handleLoadingStatus() {
    isLoading.update(isLoading => !isLoading)
  }
</script>

<svelte:head>
  <title>Home Page</title>
</svelte:head>

<div>
  <h1>Welcome to SvelteKit</h1>
  <p>
    Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
  </p>
  <button on:click={handleLoadingStatus}> Toggle Loading Status </button>
</div>

<style lang="scss">
  div {
    align-items: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
</style>
