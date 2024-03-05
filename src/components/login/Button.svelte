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
    width: 98%;
    background-color: #0073b1;
    color: white;
    border: none;
    border-radius: 25px;
    cursor: pointer;
  }
  
  .primary {
    background-color: #0073b1; 
  }
</style>
  