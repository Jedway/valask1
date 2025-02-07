<script lang="ts">
  import { push } from 'svelte-spa-router';
</script>

<div class="page">
  <img src="/src/assets/pic6.png" alt="Valentine" />
  <p>I made this to ask you a question 👉🏽👈🏽</p>
  <button on:click={() => push('/page7')}>What would that be?🧍🏾‍♀️</button>
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
    font-size: 1.5rem;
    color: #ff69b4;
    max-width: 600px;
    padding: 0 1rem;
    margin: 0;
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
    width: 90%;
    max-width: 300px;
    box-shadow: 
      0 4px 6px rgba(255, 105, 180, 0.25),
      0 6px 0 #d64d98;
    position: relative;
    top: 0;
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
      font-size: 1.2rem;
    }
    
    button {
      padding: 0.8rem 1.5rem;
      font-size: 1rem;
    }
  }
</style>