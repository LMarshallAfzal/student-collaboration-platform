<script lang="ts">
    export let label: string = '';
    export let value: string = '';
    export let placeholder: string = '';
    export let error: boolean = false; 
    export let currentType: 'text' | 'password' | 'email' = 'text';
</script>
  
<div class="input-container {error ? 'input-error' : ''}">
  <label for={label}>{label}</label>

  {#if currentType === 'text'}
      <input type="text" bind:value placeholder={placeholder}>
  {:else if currentType === 'email'}
      <input type="email" bind:value placeholder={placeholder} />
  {:else if currentType === 'password'} 
      <input type="password" bind:value placeholder={placeholder} />
  {/if}

  {#if error}
      <p class="error-message">Error: Please check your input</p>
  {/if}
</div>
  
<style>
  .input-container {
    height: 40px; 
    display: flex;
    flex-direction: column;
    margin-bottom: 5px;
    border-radius: 4px;
  }
  
  input {
    height: 40px;
    border-radius: 4px;
    border: 1px solid #000000;
    background-color: white;
    color: black;
  }

  input:hover {
    border: 2px solid #0073b1
  }
  
  .input-error input {
    border-color: red; 
  }
  
  .error-message {
    color: red;
    font-size: 0.8em;
  }
</style>
  