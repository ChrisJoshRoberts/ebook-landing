<script>
import { ChevronDown } from 'lucide-svelte';

let { question, answer, isExpanded, ...props  } = $props();
</script>

<button class="container" {...props}>
<div class="question-and-answer">
  <p class="question mb-s">{question}</p>
  <p class="answer" class:answer-expanded={isExpanded}>{answer}</p>
  <div class="chevron" class:chevron-rotated={isExpanded}>
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
  .answer-expanded {
    max-height: 100px;
    opacity: 1;
    transition: all 0.3s ease-in;
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
    transition: all 0.3s ease;
    transform: rotate(0deg);
  }
  .chevron-rotated {
    transform: rotate(180deg);
  }
  </style>