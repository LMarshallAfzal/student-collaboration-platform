<script>
  import { Router, Route } from 'svelte-routing';
  import Login from './components/login/Login.svelte';
  import Home from './components/home/Home.svelte';
  import Signup from './components/signup/Signup.svelte';
</script>

<Router>
  <Route path="/" component={Home} />
  <Route path="/login" component={Login} />
  <Route path="/signup" component={Signup} />
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
