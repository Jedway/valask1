<script lang="ts">
  import confetti from 'canvas-confetti';
  import { onMount } from 'svelte';

  let audio: HTMLAudioElement;

  onMount(() => {
    // Trigger confetti
    confetti({
      particleCount: 150,
      spread: 70,
      origin: { y: 0.6 }
    });

    // Start playing the song
    if (audio) {
      audio.play().catch(error => {
        console.log('Audio playback failed:', error);
      });
    }
  });
</script>

<div class="page">
  <img src="/assets/pic8.png" alt="Success" />
  <p>Yusssss🤲🏽 That's my girllllll😚</p>
  <!-- The audio source should be updated to point to your actual audio file -->
  <audio
    bind:this={audio}
    src="/assets/love-song.mp3"
    preload="auto"
    loop
  />
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
    background: linear-gradient(135deg, #fff5f5 0%, #ffe0e0 100%);
  }
  
  img {
    width: 100%;
    max-width: 500px;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  }
  
  p {
    font-size: 2.5rem;
    color: #ff69b4;
    max-width: 600px;
    font-weight: bold;
    padding: 0 1rem;
    margin: 0;
  }

  @media (max-width: 768px) {
    .page {
      gap: 1.5rem;
    }
    
    p {
      font-size: 1.8rem;
    }
  }
</style>