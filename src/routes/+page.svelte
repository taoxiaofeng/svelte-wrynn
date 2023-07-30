<!-- App.svelte -->
<script>
  import Layout from '../components/Layout.svelte';
</script>

<Layout title="My Backend System">
  <!-- Your sidebar content goes here -->
  <div slot="sidebar">
    <h3>Sidebar Content</h3>
    <ul>
      <li><a href="/">Home</a></li>
      <li><a href="/users">Users</a></li>
      <!-- Add more sidebar links here -->
    </ul>
  </div>

  <!-- Your page content goes here -->
  <p>Welcome to the Dashboard!</p>
</Layout>
