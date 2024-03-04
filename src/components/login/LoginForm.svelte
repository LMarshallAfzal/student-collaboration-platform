<script>
    import Input from "./Input.svelte";
    import Button from "./Button.svelte";

    // Temporarily replace handleSubmit 
    const handleSubmit = (e) => {
       e.preventDefault(); // Prevent default form submission for now
        console.log('Form submitted! (Functionality to be added later)');                         
    }
</script>

<form on:submit|preventDefault={handleSubmit}>
    <Input type="email" label="Email" />
    <Input type="password" label="Password" />
    <Button type="submit">Login</Button>
    <p class="forgot-password">Forgot Password?</p>
</form>

<style>
    form {
        background-color: white;
        padding: 30px;
        border-radius: 5px;
        box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
</style>