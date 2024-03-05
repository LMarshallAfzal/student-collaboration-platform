<script>
  import LoginForm from './components/login/LoginForm.svelte';
</script>

<div class="app-wrapper">
  <main>
      <LoginForm />   
  </main>
</div>

<style>
  .app-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    /* background-color: whitesmoke; */
    background-image: url('./assets/blue-wave-bg.jpg');
  }
</style>
