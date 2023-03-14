<script>
  // import ProjectDetail from './ProjectDetail.svelte'
   import projectsData from '../data/data.json'
   import { Link } from 'svelte-routing'

   const projects = projectsData.projects

</script>
<h1>Rapha Lobosco</h1>
<div class="container">
  {#each projects as project}
    <Link to={"/project/" + project.id}>
    <img src={project.photo} alt="">
    </Link>
  {/each}
</div>



<style>
.container {
  
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
  }

  img{
    width:100%;
  }

</style>
