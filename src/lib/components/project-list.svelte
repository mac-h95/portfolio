<script>
  import ProjectCard from "./project-card.svelte"
  export let projects
</script>

<div class="flex snap-x snap-mandatory flex-col md:items-center">
  <div
    class="flex w-screen overflow-x-auto md:flex-wrap pb-8 overflow-y-hidden justify-center slider max-w-96"
  >
    {#each projects as project}
      <ProjectCard {...project.meta} path={project.path} />
    {/each}
  </div>
</div>
