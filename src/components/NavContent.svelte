<script lang="ts">
  // Define some sample navigation items and content
  let navItems = ['Home', 'About', 'Contact'];
  let activeNavItem = navItems[0];

  let contentData: {[key:string]:string } = {
    Home: 'Welcome to our website!',
    About: 'Learn more about us.',
    Contact: 'Get in touch with us.',
  };

  // @ts-ignore
  function setActiveNavItem(item:any) {
    activeNavItem = item;
  }
</script>

<style>
  /* Style the navigation bar */
  .nav {
    display: flex;
    justify-content: space-between;
    background-color: #f0f0f0;
    padding: 10px;
  }

  .nav-item {
    cursor: pointer;
    padding: 5px 10px;
    border-bottom: 2px solid transparent;
  }

  .nav-item.active {
    border-bottom: 2px solid #007bff;
  }

  /* Style the content area */
  .content {
    margin-top: 20px;
    padding: 20px;
    border: 1px solid #ddd;
  }
</style>

<div>
  <!-- Navigation bar -->
  <div class="nav">
    {#each navItems as item}
      <div
        class={`nav-item ${activeNavItem === item ? 'active' : ''}`}
        on:click={() => setActiveNavItem(item)}
      >
        {item}
      </div>
    {/each}
  </div>

  <!-- Content area -->
  <div class="content">
    {contentData[activeNavItem]}
  </div>
</div>
