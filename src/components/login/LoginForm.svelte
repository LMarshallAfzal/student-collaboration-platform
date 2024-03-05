<script>
  import Input from "./Input.svelte";
  import Button from "./Button.svelte";
  let email = '';
  let password = ''; 
  // let currentType = "password";

  // Temporarily replace handleSubmit 
  const handleSubmit = (e) => {
      e.preventDefault(); // Prevent default form submission for now
      console.log('Form submitted! (Functionality to be added later)');                         
  }
</script>

<div class="login-container">
  <form on:submit|preventDefault={handleSubmit}>
    <h1>Sign in</h1>
    <p>Collaborate with others to unleash your academic potential</p>
    <Input currentType="email" placeholder="Email" bind:value={email}/>
    <Input currentType={"password"} placeholder="Password" bind:value={password}/>
    <a class="forgot-password" href="#">Forgot Password?</a>
    <Button type="submit">Login</Button>
    <a class="forgot-password" href="#">New to the platform? Join now</a>
  </form>
</div>

<style>
  form {
    height: 500px;
    width: 270px;
    background-color: white;
    padding: 10px;
    border-top-left-radius: 15px; 
    border-bottom-left-radius: 15px;

    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  }

  h1 {
    color: black;
    text-align: left;
    margin-top: 25px;
    margin-bottom: 2px;
  }

  p {
    color: black;
    text-align: left;
    font-size: small;
    margin-top: 3px;
    margin-bottom: 15px;
  }

  a {
    text-align: left;
    font-size: small;
    display: block;
    margin-top: 25px;
    margin-bottom: 15px;
    margin-left: 5px;
  }

  .forgot-password {
    font-weight: 700;
    color: #0073b1;
  }

  .login-container {
    background-color: white;
    width: 850px;
    border-radius: 15px;
  }
</style>