<script>
  import { Link } from 'svelte-routing';
  import Button from "../components/Button.svelte";
</script>

<div class="home-container">
  <h1>Home</h1>
  <Link to="/login">
    <Button label="Go to login"/>
  </Link>
</div>