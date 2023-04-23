<script>
  import {dev} from "$app/environment";	
  import Header from './Header.svelte';
	import PageContent from './PageContent.svelte';
	import Footer from './Footer.svelte';
	import './variables.css';
	import './main.css';
</script>

<div class="app">
	<Header />
	<main>
		<PageContent>
			<slot />
		</PageContent>
	</main>
	<Footer />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
    padding: var(--gap-xlarge) 0;
		background: var(--color-surface1);
	}

  @media (max-width: 1200px) {
    main {
      padding: var(--gap-normal) 0;
    }
  }
</style>
