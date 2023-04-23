<script>
  import Experience from "$lib/Experience.svelte";
  import ExperienceRole from "$lib/ExperienceRole.svelte";
</script>

<h3>Experience</h3>

<Experience title="Dynatrace, Linz" subTitle="Senior Software Engineer & Team Captain" link="dynatrace.com">
  <ExperienceRole start="Sept 2022" caption="Team Cloud Access Engineering, Team Captain">
    Workflows and automations for self-service tooling for all 4k+ employees worldwide.
    Managing <strong>internal access and public cloud</strong> (AWS, Azure, GCP).
    GitOps, IaC, Angular, Java/Kotlin/Spring, PostgreSQL.
  </ExperienceRole>
  <ExperienceRole start="Sept 2018" end="Sept 2022" caption="Team ACE Tooling">
    Internal tooling suite for <strong>release-, team- and access management</strong>.
    Full-stack development with Angular (v7+), Java, Spring Boot, AWS including 
    Lambda, ECS, S3, Cognito, RDS, custom SSO integration.
  </ExperienceRole>
</Experience>

<Experience title="Fusonic, Götzis" subTitle="Software Engineer" link="fusonic.net">
  <ExperienceRole start="July 2016" end="Aug 2018" caption="Web Development">
    Three <strong>customer projects</strong> in the areas of maintenance documentation and reporting as well as IoT device management, 
    offline-ready PWAs using Angular (v2+) and PHP/Symfony (MVC framework).
  </ExperienceRole>
</Experience>
