<script lang="ts">
  import confetti from 'canvas-confetti';
  import { push } from 'svelte-spa-router';
  import { onMount } from 'svelte';

  onMount(() => {
    confetti({
      particleCount: 100,
      spread: 70,
      origin: { y: 0.6 }
    });
  });
</script>

<div class="page">
  <img src="/src/assets/pic7.png" alt="Final" />
  <p>Will you be my valentine on this year of our love, 2025? ❤️</p>
  <div class="button-container">
    <button class="yes" on:click={() => push('/page8')}>Yes honey😍</button>
    <button class="no" on:click={() => push('/page8')}>Yes (Na by force😡)</button>
  </div>
</div>

<style>
  .page {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    padding: 1rem;
    text-align: center;
    min-height: 100vh;
    justify-content: center;
  }
  
  img {
    width: 100%;
    max-width: 500px;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  }
  
  p {
    font-size: 2rem;
    color: #ff69b4;
    max-width: 600px;
    font-weight: bold;
    padding: 0 1rem;
    margin: 0;
  }

  .button-container {
    display: flex;
    gap: 1rem;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;
    max-width: 600px;
    padding: 0 1rem;
  }

  button {
    background-color: #ff69b4;
    color: white;
    border: none;
    padding: 1rem 2rem;
    font-size: 1.2rem;
    cursor: pointer;
    transition: all 0.2s ease;
    border-radius: 8px;
    flex: 1;
    min-width: 200px;
    box-shadow: 
      0 4px 6px rgba(255, 105, 180, 0.25),
      0 6px 0 #d64d98;
    position: relative;
    top: 0;
  }

  button.yes {
    background-color: #ff69b4;
  }

  button.no {
    background-color: #ff69b4;
  }
  
  button:hover {
    transform: translateY(-2px);
    box-shadow: 
      0 6px 8px rgba(255, 105, 180, 0.25),
      0 8px 0 #d64d98;
  }

  button:active {
    transform: translateY(4px);
    box-shadow: 
      0 2px 4px rgba(255, 105, 180, 0.25),
      0 2px 0 #d64d98;
  }

  @media (max-width: 768px) {
    .page {
      gap: 1.5rem;
    }
    
    p {
      font-size: 1.5rem;
    }

    button {
      padding: 0.8rem 1.5rem;
      font-size: 1rem;
      min-width: 150px;
    }
  }
</style>