<!-- HeadContent.svelte -->

<script>
  export let isDark = false;
  export let toggleTheme = () => {};
</script>

<header>
  <h1>Hello Svelte!</h1>
  <button on:click={toggleTheme}>Toggle Theme</button>
</header>

<style>
  header {
    background-color: #f0f0f0;
    padding: 20px;
    text-align: center;
  }

  /* Add styles for the dark theme */
  :global(body.dark) header {
    background-color: #333;
    color: #fff;
  }
</style>
