<script lang="ts">
  import { createEventDispatcher } from 'svelte';
  import { base } from '$app/paths';

  export let type: 'raised' | 'flat' = 'raised';
  export let link: string | undefined = undefined;
  export let isExternal: boolean = false;

  const dispatch = createEventDispatcher();
  function handleClick() {
    dispatch('click');
  }
</script>

{#if link}
  <a class={`button ${type}`} href={link} target={isExternal ? '_blank' : ''} rel={isExternal ? 'noreferrer' : ''}>
    <slot />
  </a>
{:else}
  <button class={`button ${type}`} on:click={handleClick}>
    <slot />
  </button>
{/if}

<style>
  .button {
    padding: var(--gap-normal) var(--gap-large);
    color: var(--color-text1);
    border: 1px solid transparent;
    border-radius: var(--border-radius);
    user-select: none;
    cursor: pointer;
  }

  .button.flat {
    color: var(--color-primary);
  }

  .button.raised {
    text-decoration: none;
    border-color: var(--color-border1);
    background: var(--color-surface4);
  }

  .button.raised:hover {
    background: var(--color-surface3);
  }

  @media (min-width: 1200px) {
    .button.raised {
      padding: var(--gap-small) var(--gap-normal);
      font-size: var(--font-size-smaller);
    }
  }
</style>

