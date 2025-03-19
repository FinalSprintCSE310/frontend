<script>
import {Router, Link, Route } from 'svelte-routing';

import Home from '../../routes/Home.svelte';
import About from '../../routes/About.svelte';
import Login from '../../routes/Login.svelte';
</script>

<style>
  h1 {
    padding: 20px;
    font-weight: bold;
    background-color: #fffbfb;
  }
  nav {
    display: left;
    justify-content: space-around;
    align-items: center;
    padding-left: 10px;
    border-top: 1px solid #000000;
    border-bottom: 1px solid #000000;
    background-color: #fffbfb;
  }
  .footer {
        position: absolute;
        bottom: 0;
      text-align: right;
      padding: 10px;
      border-top: 1px solid #000000;
      width: 100vw;
    }
  </style>
  <h1>Cantva</h1>
<Router>
    <nav class="text-2xl text-blue-500">
    <Link to="/">Home</Link>
    <Link to="/about">About</Link>
    <Link to="/login">Login</Link>
</nav>
<div>
    <Route path="/"> <Home/> </Route>
    <Route path="/about/:id" let:params> <About id="{params.id}"/> </Route>
    <Route path="/login"> <Login /> </Route>
</div>

  <!-- Footer -->
  <div class="footer">
    <p>© 2025 Schooled Systems</p>
  </div>
</Router>