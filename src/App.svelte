<script lang="ts">
  import Router from 'svelte-spa-router';
  import Page1 from './routes/Page1.svelte';
  import Page2 from './routes/Page2.svelte';
  import Page3 from './routes/Page3.svelte';
  import Page4 from './routes/Page4.svelte';
  import Page5 from './routes/Page5.svelte';
  import Page6 from './routes/Page6.svelte';
  import Page7 from './routes/Page7.svelte';
  import Page8 from './routes/Page8.svelte';

  const routes = {
    '/': Page1,
    '/page2': Page2,
    '/page3': Page3,
    '/page4': Page4,
    '/page5': Page5,
    '/page6': Page6,
    '/page7': Page7,
    '/page8': Page8
  };
</script>

<main>
  <Router {routes} />
  <footer>
    <p>© 2025 For The Love Of My Life.</p>
  </footer>
</main>

<style>
  main {
    min-height: 100vh;
    background: linear-gradient(135deg, #fff5f5 0%, #ffe0e0 100%);
    position: relative;
    padding-bottom: 60px; /* Space for footer */
  }

  footer {
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    background: rgba(255, 255, 255, 0.9);
    backdrop-filter: blur(5px);
    padding: 1rem;
    text-align: center;
    box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
  }

  footer p {
    margin: 0;
    color: #ff69b4;
    font-size: 0.9rem;
    font-family: 'Inter', sans-serif;
  }
</style>