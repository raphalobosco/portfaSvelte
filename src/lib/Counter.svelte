<script>
  export let title
  export let photo 
  export let desc 

</script>

<div>
  <h2>{title}</h2>
  <p>{desc}</p>
  <img src={photo} alt="">
</div>

<style>
img{
  display: block;
  min-width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 1rem;
}
</style>
