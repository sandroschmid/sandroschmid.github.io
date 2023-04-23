<script lang="ts">
  export let category: string | undefined = undefined;
  export let label: string | undefined = undefined;
</script>

<div class="skill-item">
  {#if category && category.length > 0}
    <div class="font-caption">{category}</div>
  {/if}
  {#if label && label.length > 0}
    <span class="font-text2">{label}:</span>
  {/if}
  <slot />
</div>

<style>
  .skill-item {
    padding: var(--gap-normal);
    background: var(--color-surface3);
    border-radius: var(--border-radius);
  }

  .skill-item:not(:first-of-type) {
    margin-top: var(--gap-large);
  }
</style>
