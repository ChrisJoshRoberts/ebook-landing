<script>
  let { children, ...props } = $props();
</script>

<button {...props} class="white button">{@render children()}</button>

<style>
  .button {
    border: 1px solid white;
    background-color: transparent;
    width: 25%;
    padding: 1rem 0;
    font-size: 1rem;
    margin-top: 1rem;
    transition: all 0.3s ease;
    cursor: pointer;

    &:hover {
      background-color: white;
      color: black;
    }
  }
</style>