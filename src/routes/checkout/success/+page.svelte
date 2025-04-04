<script>
  import HeroSection from "$components/HeroSection.svelte";

  const handleClick = () => {
    window.location.href = "/";
  };
</script>


<HeroSection>
  <h1>Thank you for purchasing!</h1>
  <button onclick={handleClick}>Back Home</button>
</HeroSection>

<style>
  button {
    background-color: transparent;
    border: 1px solid white;
    color: white;
    width: 25%;
    padding: 1rem 0;
    font-size: 1rem;
    margin-top: 1rem;
    transition: all 0.3s ease;
    cursor: pointer;

    &:hover {
      background-color: white;
      color: black;
      border: 1px solid black;
    }
  }
</style>