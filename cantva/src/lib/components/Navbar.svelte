<script>
import {Router, Link, Route } from 'svelte-routing';

import Home from '../../routes/Home.svelte';
import About from '../../routes/About.svelte';
</script>
<Router>
    <nav>
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
</nav>
<div>
    <Route path="/"> <Home/> </Route>
    <Route path="/about/:id" let:params> <About id="{params.id}"/> </Route>
    <Route path="/"> <Home /> </Route>
</div>
</Router>