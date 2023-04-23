<script lang="ts">
  import Link from "$lib/Link.svelte";

  export let title: string | undefined = undefined;
  export let subTitle: string | undefined = undefined;
  export let link: string | undefined = undefined;
  export let linkLabel: string | undefined = undefined;
  
  const href = link && !link.startsWith('http') ? `https://${link}` : link;
</script>

<div class="experience">
  {#if link}
    <div class="font-small">
      <Link link={href} isExternal>
        {#if linkLabel}
          {linkLabel}
        {:else}
          www.{link}
        {/if}
      </Link>
    </div>
  {/if}
  <h4>
    {title}
    {#if subTitle}
    &mdash; {subTitle}
    {/if}
  </h4>

  <slot />
</div>

<style>
  h4 {
    margin: var(--gap-normal) 0 var(--gap-large);
  }

  .experience {
    padding: var(--gap-normal);
    background: var(--color-surface2);
    border-radius: var(--border-radius);
  }

  .experience:not(:first-of-type) {
    margin-top: var(--gap-large);
  }
</style>
