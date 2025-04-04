<script>
  import { FaqItem } from "$components";
	import Button from "./Button.svelte";

  const faqs = [
  {
    question: "What is the best way to learn JavaScript?",
    answer: "The best way to learn JavaScript is through hands-on practice, building projects, and studying resources like MDN, freeCodeCamp, and JavaScript.info."
  },
  {
    question: "How do I improve website performance?",
    answer: "Optimize images, minify CSS and JavaScript, enable lazy loading, use a CDN, and leverage browser caching to improve website performance."
  },
  {
    question: "What is the difference between let, const, and var?",
    answer: "let and const are block-scoped, while var is function-scoped. const cannot be reassigned, whereas let can be updated but not re-declared."
  },
  {
    question: "How does React handle state management?",
    answer: "React manages state using the useState hook for local state, and tools like Context API, Redux, or Zustand for global state management."
  },
  {
    question: "What is Next.js used for?",
    answer: "Next.js is a React framework for building server-rendered applications, static sites, and API routes with improved SEO and performance."
  },
  {
    question: "How can I deploy a web application?",
    answer: "You can deploy a web application using services like Vercel, Netlify, AWS, or DigitalOcean, depending on your needs and infrastructure."
  }
];

let questionCurrentlyExpanded = $state(-1);

const toggleQuestion = (index) => {
  questionCurrentlyExpanded = index;
};

</script>

<section class="faq-section"> 
  <h2 class="mb-l">Frequently Asked Questions</h2>
  <div class="faq-container">
    {#each faqs as faq, index}
      <FaqItem 
        question={faq.question} 
        answer={faq.answer} 
        isExpanded={index === questionCurrentlyExpanded} 
        onclick={() => toggleQuestion(index)}
      />
    {/each}
  </div>
  <div class="additional-info mt-m">
    <Button mode='dark'>
      BUY NOW
    </Button>
    <p class="mt-s">Any other questions?</p>
    <a href="https://x.com">
      <p>Hit me up on X</p>
    </a>
  </div>
</section>

<style>
  .faq-section {
    padding: 80px 0;
    margin: 0 auto;
    max-width: 1200px;
  }
  .additional-info {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
</style>