<script>
import { ChevronDown } from 'lucide-svelte';

let { question, answer } = $props();
</script>

<button class="container">
<div class="question-and-answer">
  <p class="question mb-s">{question}</p>
  <p class="answer">{answer}</p>
  <div class="chevron">
    <ChevronDown />
  </div>
</div>
</button>

<style>
  .container {
    width: 100%;
  }
  .question {
    padding-top: 16px;
    font-size: 1.5rem;
    font-weight: bold;
  }
  .answer {
    text-align: left;
    font-size: 1rem;
    color: #555;
    padding-right: 2rem;
    max-height: 0;
    overflow: hidden;
    opacity: 0;
    transition: all 0.3s ease-out;
  }
  .question-and-answer {
    display: flex;
    padding: 8px 0px;
    position: relative;
    flex-direction: column;
    align-items: flex-start;
    border-bottom: 1px solid #222020;
  }
  .chevron {
    display: flex;
    align-items: center;
    position: absolute;
    right: 0;
    height: 100%;
  }
</style>