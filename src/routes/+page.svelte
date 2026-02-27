<script>
  let count = $state(0);
</script>

<div class="app">
  <header>
    <div class="logo">
      <svg width="40" height="40" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <polygon points="12 2 22 8.5 22 15.5 12 22 2 15.5 2 8.5 12 2" />
        <line x1="12" y1="22" x2="12" y2="15.5" />
        <polyline points="22 8.5 12 15.5 2 8.5" />
      </svg>
    </div>
    <h1>SvelteKit</h1>
    <p class="subtitle">Deployed with <a href="https://ml.ink" target="_blank" rel="noopener noreferrer">Ink</a></p>
  </header>

  <main>
    <div class="card">
      <button onclick={() => count++}>
        Count is {count}
      </button>
      <p class="hint">Click the button to test reactivity</p>
    </div>

    <div class="links">
      <a href="https://svelte.dev" target="_blank" rel="noopener noreferrer">Svelte Docs</a>
      <a href="https://svelte.dev/docs/kit" target="_blank" rel="noopener noreferrer">SvelteKit Docs</a>
      <a href="https://docs.ml.ink" target="_blank" rel="noopener noreferrer">Ink Docs</a>
    </div>
  </main>
</div>

<style>
  :global(*),
  :global(*::before),
  :global(*::after) {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  :global(body) {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    background: #0a0a0a;
    color: #ededed;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .app {
    text-align: center;
    padding: 2rem;
    max-width: 600px;
  }

  header {
    margin-bottom: 3rem;
  }

  .logo {
    color: #ff3e00;
    margin-bottom: 1.5rem;
  }

  h1 {
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 0.5rem;
  }

  .subtitle {
    color: #888;
    font-size: 1.1rem;
  }

  .subtitle a {
    color: #ff3e00;
    text-decoration: none;
  }

  .subtitle a:hover {
    text-decoration: underline;
  }

  .card {
    margin-bottom: 2.5rem;
  }

  button {
    background: #1a1a2e;
    color: #ededed;
    border: 1px solid #333;
    border-radius: 8px;
    padding: 0.75rem 1.5rem;
    font-size: 1rem;
    cursor: pointer;
    transition: border-color 0.2s, background 0.2s;
  }

  button:hover {
    border-color: #ff3e00;
    background: #2e1a1a;
  }

  .hint {
    margin-top: 0.75rem;
    color: #666;
    font-size: 0.85rem;
  }

  .links {
    display: flex;
    gap: 1.5rem;
    justify-content: center;
  }

  .links a {
    color: #888;
    text-decoration: none;
    font-size: 0.9rem;
    transition: color 0.2s;
  }

  .links a:hover {
    color: #ff3e00;
  }
</style>
