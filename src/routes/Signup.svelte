<script>
  import SignupForm from "../components/signup/SignupForm.svelte";
</script>

<div class="app-wrapper">
  <main>
    <SignupForm />
  </main>
</div>

<style>
  .app-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    /* background-color: whitesmoke; */
    background-image: url("../assets/blue-wave-bg.jpg");
  }
</style>
