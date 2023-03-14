<script>

  import { Router, Route } from 'svelte-routing'
  import Home from './pages/Home.svelte'
  import Details from './pages/Details.svelte'


</script>
<div class="container">
<Router>
    <Route component="{Home}" />
    <Route path="/project/:id" let:params>
        <Details {...params} />
    </Route> 
</Router>
</div>

<style>

</style>
