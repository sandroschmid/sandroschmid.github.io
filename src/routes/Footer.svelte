<script lang="ts">
  import Link from "$lib/Link.svelte";
	import PageContent from './PageContent.svelte';
  
  const now = new Date();
  const year = now.getUTCFullYear();
  const month = now.getUTCMonth();
</script>

<footer>
  <PageContent>
    &copy; Sandro Schmid, {month < 10 ? `0${month}` : month}/{year} | Built with 🧡 <Link link='https://svelte.dev/' isExternal>Svelte</Link>
  </PageContent>
</footer>

<style>
	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: var(--gap-normal) var(--gap-large);
    font-size: var(--font-size-small);
	  text-align: center;
	}
</style>
