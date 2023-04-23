<script lang="ts">
  import { derived } from 'svelte/store';
  import { page } from '$app/stores';
  import Button from "$lib/Button.svelte";

  let isNotFound = derived(page, $p => $p.status === 404);
</script>

<h2>{$page.status} {$page.error.message}</h2>

<section>
  <p>
    {#if $isNotFound}
      I am afraid this page does not exist 😔
    {:else}
      I am sorry, something unexpected happened 😔
    {/if}
  </p>
</section>

<section>
  <Button link="/">View homepage</Button>
</section>
