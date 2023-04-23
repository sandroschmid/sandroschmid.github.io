<script lang="ts">
  import Link from "$lib/Link.svelte";
  export let badges: object[] = [];

  const credlyUrl = (id: string) => `https://www.credly.com/badges/${id}/public_url`;
  const credlyTooltip = (name: string) => `View '${name}' on Credly`;
</script>

<div class="badges">
  {#each badges as badge}
    <Link link={credlyUrl(badge.id)} isExternal>
      <div class="badge" title={credlyTooltip(badge.name)}>
        <img src={badge.imageSrc} alt={badge.name}>
        <span>{badge.name}</span>
      </div>
    </Link>
  {/each}
</div>

<style>
  .badges {
    display: grid;
    grid-template-columns: repeat(1, 250px);
    justify-content: center;
    align-content: center;
  }

  .badge {
    display: inline-flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: var(--gap-normal);
    font-size: var(--font-size-smaller);
  }

  img {
  	max-width: 150px;
  }
</style>
