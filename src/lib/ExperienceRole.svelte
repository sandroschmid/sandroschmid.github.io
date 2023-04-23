<script lang="ts">
  export let start: string | undefined = undefined;
  export let end: string | undefined = undefined;
  export let caption: string | undefined = undefined;
</script>

<div class="experience-role">
  {#if caption && caption.length > 0}
  <div class="font-small">{caption}</div>
  {/if}
  <div class="font-small">{start} &dash; {end || 'PRESENT'}</div>

  <p>
    <slot />
  </p>
</div>

<style>
  .experience-role {
    margin-top: var(--gap-small);
    padding: var(--gap-normal);
    background: var(--color-surface3);
    border-radius: var(--border-radius);
  }
  
  .experience-role:first-of-type {
    margin-top: var(--gap-normal);
  }

  .experience-role:not(:first-of-type) {
    margin-top: var(--gap-small);
  }
</style>
