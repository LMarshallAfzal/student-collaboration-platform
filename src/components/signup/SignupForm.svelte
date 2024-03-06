<script>
  import Input from "../Input.svelte";
  import Button from "../Button.svelte";
  
  let name = ""
  let email = "";
  let password = "";
  let passwordConfirmation = "";

  // Temporarily replace handleSubmit
  const handleSubmit = (e) => {
    e.preventDefault(); // Prevent default form submission for now
    console.log("Form submitted! (Functionality to be added later)");
  };
</script>

<div class="login-container">
  <form on:submit|preventDefault={handleSubmit}>
    <h1>Sign up</h1>
    <p>Collaborate with others to unleash your academic potential</p>
    <Input 
      currentType="text" 
      placeholder="Name"
      bind:value={name} 
    /> 
    <Input 
      currentType="email" 
      placeholder="Email" 
      bind:value={email} 
    />
    <Input
      currentType={"password"}
      placeholder="Password"
      bind:value={password}
    />
    <Input
      currentType={"password"}
      placeholder="Password Confirmation"
      bind:value={passwordConfirmation}
    />
    <a class="forgot-password" href="#">Forgot Password?</a>
    <Button label="Submit" type="submit" />
    <a class="forgot-password" href="/login">Have an account already? Sign in</a>
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

    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
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
    background-image: url("../../assets/3948.jpg");
    background-size: cover;
    width: 850px;
    border-radius: 15px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
</style>
