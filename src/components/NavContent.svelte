<!-- NavContent.svelte -->

<script>
  export let isDark;
</script>

<nav>
  <ul>
    <li>Home</li>
    <li>About</li>
    <li>Contact</li>
  </ul>
</nav>

<style>
  nav {
    background-color: #f0f0f0;
    padding: 10px;
  }

  ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
  }

  li {
    display: inline-block;
    margin-right: 10px;
    cursor: pointer;
  }

  /* Add styles for the dark theme */
  :global(body.dark) nav {
    background-color: #333;
    color: #fff;
  }
</style>