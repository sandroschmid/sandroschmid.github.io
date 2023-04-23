<script lang="ts">
export let tags: string[] = [];
</script>

<ul>
  {#each tags as tag}
		<li>
			{tag.toLowerCase().replaceAll(/[^\w]/g, "-")}
		</li>
	{/each}
</ul>

<style>
  ul {
    max-width: calc(var(--max-page-width) / 2);
    margin: 0 auto;
    padding: 0;
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    gap: var(--gap-normal);
    justify-content: center;
    line-height: 1rem;
  }
  
  li {
    color: var(--color-primary);
    font-size: var(--font-size-smaller);
    font-family: var(--font-mono);
  }
  
  li::before {
    content: '#';
    color: var(--color-text1);
    font-size: var(--font-size-small);
  }
</style>
