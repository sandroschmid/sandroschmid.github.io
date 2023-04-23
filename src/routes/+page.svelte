<svelte:head>
	<title>Sandro Schmid</title>
	<meta name="description" content="Sandro Schmid's personal website." />
</svelte:head>

<script lang="ts">
  import TagList from "$lib/TagList.svelte";
  import Button from "$lib/Button.svelte";
  import CredlyBadge from "$lib/CredlyBadge.svelte";
  import imgAwsDev from "$lib/images/aws-certified-developer-associate.png";

  const tags: string[] = [
    'Software Engineering',
    'Angular',
    'AWS',
    'Java',
    'Spring Boot',
    'Auth',
    'Cloud',
    'SQL',
  ];

  const links: {label: string, href: string}[] = [
    {label: 'LinkedIn', href: 'https://www.linkedin.com/in/sandro-schmid/'},
    {label: 'GitHub', href: 'https://github.com/sandroschmid/'},
    {label: 'StackOverflow', href: 'https://stackoverflow.com/users/3863059/sschmid'},
  ];

  const badges = [
    {
      name: 'AWS Certified Developer – Associate',
      id: '106108f6-0e5a-4336-b0b1-43d8abdf3804',
      imageSrc: imgAwsDev
    }
  ]
</script>

<div class="home">
  <section>
    <h2>Hi there 👋</h2>
    <p>I am a Senior Software Engineer and Team Lead located in Austria. I do full stack web-engineering and cloud things.</p>
  </section>

  <section>
    <TagList tags={['Software Engineering', 'Cloud', 'AWS']} />
    <TagList tags={['Java', 'Kotlin', 'Spring Boot', 'Auth', 'SQL']} />
    <TagList tags={['TypeScript', 'Angular']} />
  </section>

  <section>
    <p>You can find me online&hellip;</p>
    <div class="button-group">
      {#each links as link}
        <Button link={link.href} isExternal>{link.label}</Button>
      {/each}
    </div>
  </section>

  <section>
    <CredlyBadge {badges} />  
  </section>
</div>

<style>
  .home {
	  text-align: center;
    max-width: calc(var(--max-page-width) * 0.5);
    margin: 0 auto;
  }

  .button-group {
    display: flex;
    flex-wrap: wrap;
    gap: var(--gap-normal);
    justify-content: center;
  }
</style>
