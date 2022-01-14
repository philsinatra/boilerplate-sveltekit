<script lang="ts">
  import '../scss/app.scss'
  import { isLoading } from '../stores'
  import Nav from '$lib/Nav.svelte'

  let loading

  isLoading.subscribe(value => {
    loading = value
  })
</script>

{#if loading}
  <p>Loading...</p>
{:else}
  <Nav />
{/if}

<slot />
