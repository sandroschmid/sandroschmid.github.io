<script lang="ts">
  import { base } from '$app/paths';

  export let link: string | undefined = undefined;
  export let isExternal: boolean = false;
</script>

<a href={link} target={isExternal ? '_blank' : ''} rel={isExternal ? 'noreferrer' : ''}>
  <slot />
</a>

<style>
  a {
    font-family: var(--font-mono);
    user-select: none;
  }
</style>