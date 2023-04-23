<script>
  import Link from "$lib/Link.svelte";
  import TagList from "$lib/TagList.svelte";
  import SkillItem from "./SkillItem.svelte";
</script>

<h4>Skills</h4>
<TagList tags={['Full stack', 'web development']}></TagList>
<TagList tags={['TypeScript', 'Angular', 'NgRx', 'd3.js']}></TagList>
<TagList tags={['Java', 'Kotlin', 'Spring Boot']}></TagList>
<TagList tags={['MySQL', 'PostgreSQL', 'ElasticSearch']}></TagList>
<TagList tags={['Team player', 'self-driven', 'looking ahead']}></TagList>

<h4>Projects</h4>
<SkillItem category="Developer experience & efficiency" label="ACEpresso">
  Angular app-shell and component-library including auth and SSO integration for internal
  tooling at <Link link="https://dynatrace.com" isExternal>Dynatrace</Link>.
</SkillItem>
<SkillItem category="Bachelor thesis" label="NormalizedDB">
  Add normalization to IndexedDB, the NoSQL document store for offline-ready PWAs
  (<Link link="https://github.com/normalized-db" isExternal>GitHub</Link>).
</SkillItem>

<h4>Awards</h4>
<SkillItem category="Android, Logistics" label="Digital Business Award 2015">
  Android app to optimize real-time communication in global supply chains; in collaboration with
  <Link link="https://www.alpegagroup.com/en/tms/inet/" isExternal>inet Logistics</Link>.
</SkillItem>

<h4>Languages</h4>
<TagList tags={['German', 'English']}></TagList>
