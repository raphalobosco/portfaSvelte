<script>
import projectsData from '../data/data.json'
   import { Link } from 'svelte-routing'


  export let id

  const data = projectsData.projects
  const project = data.find(project => project.id)

</script>

<div class="single-proj">
            <div class="side">
                <div class="info">
                    <h1> {project.title} </h1>
                    <p>{project.desc}</p>
                    <Link to="/">Back</Link>
                </div>
            </div>
            <div>
            {#each project.images as index}
                
                    <img src={index} key={index} alt="" />
             {/each}
            </div>
        </div >




<style lang="scss" scoped >

</style>
