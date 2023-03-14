<script>
  // import ProjectDetail from './ProjectDetail.svelte'
   import projectsData from '../data/data.json'
   import { Link } from 'svelte-routing'

   const projects = projectsData.projects

</script>
<h1>Rapha Lobosco</h1>
<div class="container">
  <div class="projects-grid">
    {#each projects as project}
      <Link to={"/project/" + project.id}>
      <div class="item">
      <img src={project.photo} alt="">
        <div class="info">
            <p class="title">{project.title}</p>
            <p class="category">UX, UI</p>
        </div>
      </div>
      </Link>
    {/each}
  </div>
</div>



<style lang="scss">

</style>
