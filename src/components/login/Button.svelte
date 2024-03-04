<script lang="ts">
  export let label: string = 'Submit';
  export let type: 'button' | 'submit' | 'reset' = 'button';
  export let primary: boolean = true;  
</script>
  
<button type={type} class:primary>
    {label}
</button>
  
<style>
  button {
    padding: 10px 20px;
    background-color: #0073b1; /* LinkedIn blue */
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .primary {
    background-color: #0073b1; 
  }
</style>
  