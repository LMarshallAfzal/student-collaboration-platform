<script lang="ts">
    export let label: string = '';
    export let value: string = '';
    export let placeholder: string = '';
    export let error: boolean = false; 
    export let type: 'text' | 'password' | 'email' = 'text';
</script>
  
<div class="input-container {error ? 'input-error' : ''}">
  <label for={label}>{label}</label>
  {#if type === 'text'}
      <input type="text" bind:value placeholder={placeholder}>
  {:else if type === 'password'}
      <input type="password" bind:value placeholder={placeholder}>
  {/if}

  {#if error}
      <p class="error-message">Error: Please check your input</p>
  {/if}
</div>
  
<style>
  .input-container { 
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
  }
  
  input {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  .input-error input {
    border-color: red; 
  }
  
  .error-message {
    color: red;
    font-size: 0.8em;
  }
</style>
  