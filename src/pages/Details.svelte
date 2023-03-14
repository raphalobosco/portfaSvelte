<script>
import projectsData from '../data/data.json'
   import { Link } from 'svelte-routing'


  export let id

  const data = projectsData.projects
  const project = data.find(project => project.id)

</script>

<div>

<h1>{project.title} {id} </h1>
  <p>{project.desc}</p>
  <img src={project.photo} alt="">
</div>

<Link to="/">Back</Link>

<style>
img{
  display: block;
  min-width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 1rem;
}
</style>
