<script>
  import Input from "../Input.svelte";
  import Button from "../Button.svelte";
  import { user } from "../../lib/stores";
  import { supabase } from "../../lib/supabaseClient";
  let email = "";
  let password = "";

  const handleSubmit = async () => {
    try {
      let { data, error } = await supabase.auth.signInWithPassword({
        email,
        password,
      })
      if (error) throw error;

      $user = data.user;
    } catch (error) {
      console.error("Login Error: ", error.message)
    }
  };
</script>

<div class="login-container">
  <form on:submit|preventDefault={handleSubmit}>
    <h1>Sign in</h1>
    <p>Collaborate with others to unleash your academic potential</p>
    <Input currentType="email" placeholder="Email" bind:value={email} />
    <Input
      currentType={"password"}
      placeholder="Password"
      bind:value={password}
    />
    <a class="forgot-password" href="#">Forgot Password?</a>
    <Button label="Submit" type="submit" />
    <a class="forgot-password" href="/signup">New to the platform? Join now</a>
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
