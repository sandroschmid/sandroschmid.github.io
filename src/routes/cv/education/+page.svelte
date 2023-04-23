<script>
  import Experience from "$lib/Experience.svelte";
  import ExperienceRole from "$lib/ExperienceRole.svelte";
  import Link from "$lib/Link.svelte";
</script>

<h3>Education</h3>

<Experience title="Human Centered Computing (MSc)" linkLabel="www.fh-ooe.at/se"
  link="https://www.fh-ooe.at/en/hagenberg-campus/studiengaenge/master/human-centered-computing/">
  <ExperienceRole start="Sept 2018" end="Sept 2020" caption="University of Applied Sciences, Upper Austria, FH Hagenberg">
    Cross-domain Software Engineering including Human-Machine interaction, psychology, UI/UX, Design Thinking.
    <strong>Master thesis</strong>: Interactive network visualization and exploration for AWS VPC Flow Logs,
    using ElasticSearch and Angular/d3.js. Cooperation with 
    <Link link="https://dynatrace.com" isExternal>Dynatrace</Link>.
  </ExperienceRole>
</Experience>

<Experience title="Software Engineering (BSc)" linkLabel="www.fh-ooe.at/hcc"
  link="https://www.fh-ooe.at/en/hagenberg-campus/studiengaenge/bachelor/software-engineering/">
  <ExperienceRole start="Sept 2015" end="July 2018" caption="University of Applied Sciences, Upper Austria, FH Hagenberg">
    Computer science foundations, algorithms, data structures, end-to-end software lifecycle and project management.
    <strong>Bachelor thesis</strong>: Normalization in document stores, especially IndexedDB. Cooperation with
    <Link link="https://fusonic.net" isExternal>Fusonic</Link>.
  </ExperienceRole>
</Experience>

<Experience title="Business Academie, Digital Business (A-levels)" linkLabel="hak-bregenz.ac.at/hwi-allgemein"
  link="https://www.hak-bregenz.ac.at/hwi-allgemein/">
  <ExperienceRole start="Sept 2010" end="June 2015">
    Business foundations like economics and accounting but also programming and software engineering: .NET/C# and Entity Framework, MySQL, PHP, JavaScript.
    <strong>A-levels project</strong>: native app development with Java and Angular using Google services (now Firebase),
    awarded with the <strong>Digital Business Award 2015</strong>.
  </ExperienceRole>
</Experience>

