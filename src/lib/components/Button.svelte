<script>
  import { loadStripe } from '@stripe/stripe-js'
  import { PUBLIC_STRIPE_KEY } from '$env/static/public';
	import { goto } from '$app/navigation';


  let { children, mode,  ...props } = $props();

  const handleClick = async() => {
    try {
      const stripe = await loadStripe(PUBLIC_STRIPE_KEY);
    const response =  await fetch("/api/checkout", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
      },
    })
    const { sessionId } = await response.json();
    await stripe?.redirectToCheckout({sessionId})
    } catch (error) {
      console.error("Error:", error);
      goto('/checkout/cancel');
    }

  }
</script>

<button onclick={handleClick} {...props} class={mode === 'dark' ? 'button-dark' : 'white button'}>{@render children()}</button>

<style>
  .button-dark {
    border: 1px solid white;
    background-color: black;
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