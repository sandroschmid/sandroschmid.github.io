<script lang="ts">
  import { createEventDispatcher } from 'svelte';
  import { base } from '$app/paths';

  export let link: string | undefined = undefined;
  export let isExternal: boolean = false;

  const dispatch = createEventDispatcher();
  function handleClick() {
    dispatch('click');
  }
</script>

{#if link}
  <a class="button" href={link} target={isExternal ? '_blank' : ''} rel={isExternal ? 'noreferrer' : ''}>
    <slot />
  </a>
{:else}
  <button class="button" on:click={handleClick}>
    <slot />
  </button>
{/if}

<style>
  .button {
    padding: var(--gap-normal) var(--gap-large);
    color: var(--color-text1);
    background: var(--color-surface4);
    border: 1px solid var(--color-border1);
    border-radius: var(--border-radius);
    text-decoration: none;
    user-select: none;
  }

  .button:hover {
    cursor: pointer;
    background: var(--color-surface3);
  }

  @media (min-width: 1200px) {
    .button {
      padding: var(--gap-small) var(--gap-normal);
      font-size: var(--font-size-smaller);
    }
  }
</style>

