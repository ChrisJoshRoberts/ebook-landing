<script>
  import { Button } from "$components";
  import HeroSection from "$components/HeroSection.svelte";
</script>


<HeroSection>
  <h1>Error While Purchasing</h1>
  <div class="btn-container">
    <Button mode="light">Try Again</Button>
    <button onclick={() => window.location.href = "/"}>Go Home</button>
  </div>
</HeroSection>

<style>
  .btn-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
  }
  button {
    background-color: transparent;
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
    }
  }
</style>