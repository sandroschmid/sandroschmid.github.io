<script>
  import Skills from './Skills.svelte';
</script>

<div class="app">
  <section class="text-center">
    <h2>Curiculum Vitae</h2>
    <p>Passionate for full-stack Web Engineering and Cloud.</p>
  </section>
  <section class="cv">
    <article>
      <slot />
    </article>
    <aside>
      <Skills />
    </aside>
  </section>
</div>

<style>
	.cv {
		display: flex;
    flex-direction: column;
    gap: var(--gap-xlarge);
	}

  article {
    flex: 3;
  }

  aside {
    flex: 1;
    min-width: 360px;
  }
  
  @media (min-width: 1200px) {
    .cv {
      flex-direction: row;
      flex-wrap: wrap;
    }

    aside {
      font-size: var(--font-size-smaller);
    }
  }
</style>
