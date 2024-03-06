<script>
  import { Router, Route } from 'svelte-routing';
  import Login from './routes/Login.svelte';
  import Home from './routes/Home.svelte';
  import Signup from './routes/Signup.svelte';
  import Dashboard from './routes/Dashboard.svelte';
</script>

<Router>
  <Route path="/" component={Home} />
  <Route path="/login" component={Login} />
  <Route path="/signup" component={Signup} />
  <Route path="/dashboard" component={Dashboard} />
</Router>

<!-- <style>
  .app-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    /* background-color: whitesmoke; */
    background-image: url('./assets/blue-wave-bg.jpg');
  }
</style> -->
