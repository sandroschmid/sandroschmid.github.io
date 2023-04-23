<script>
	import Avatar from '$lib/Avatar.svelte';
  import PageContent from './PageContent.svelte';

  const avatar = {
    src: 'https://avatars.githubusercontent.com/u/18055485',
    alt: 'Avatar Sandro Schmid',
  }
</script>

<header>
  <PageContent>
    <Avatar src={avatar.src} alt={avatar.alt} />  
    <h1>Sandro S. Schmid</h1>
  </PageContent>
</header>

<style>
  header {
    padding: var(--gap-xlarge) 0;
  	background: var(--color-surface4);
  }
  
  @media (max-width: 1200px) {
    header {
      padding: var(--gap-normal) 0;
    }
  }
</style>
