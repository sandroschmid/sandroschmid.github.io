<script>
	import Avatar from '$lib/Avatar.svelte';
  import Button from '$lib/Button.svelte';
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
    <nav>
      <Button type="flat" link="/">About me</Button>
      <Button type="flat" link="/cv/experience">Experience</Button>
      <Button type="flat" link="/cv/education">Education</Button>
    </nav>
  </PageContent>
</header>

<style>
  header {
    padding: var(--gap-xlarge) 0;
  	background: var(--color-surface4);
	  text-align: center;
  }

  header nav {
    font-size: var(--font-size-large);
  }
  
  @media (max-width: 1200px) {
    header {
      padding: var(--gap-normal) 0;
    }
  }
</style>
