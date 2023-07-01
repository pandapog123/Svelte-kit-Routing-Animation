<svelte:head>
  <style>
    head,
    body {
      margin: 0;
    }
  </style>
</svelte:head>

<header>
  <a href="/left">Left Page</a>
  <a href="/">Main Page</a>
  <a href="/right">Right Page</a>
</header>

<div class="animation-container">
  <slot />
</div>

<style>
  header {
    padding: 0.5rem;
    display: flex;
    justify-content: space-between;
  }

  .animation-container {
    display: flex;
    justify-content: center;
    margin: 10rem;
  }

  a {
    text-decoration: none;
    font-size: 1.5rem;
    border-radius: 1rem;
    padding: 0.8rem;
    color: white;
    background-color: cadetblue;
    transition: all 150ms ease-in-out;
  }

  a:active {
    background-color: deepskyblue;
  }
</style>
