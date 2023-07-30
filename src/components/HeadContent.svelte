<script>
  // Props
  export let title = 'Default Title';
  export let content = 'Default content goes here.';
</script>

<style>
  /* Style the header section */
  .header {
    background-color: #007bff;
    color: white;
    padding: 20px;
    text-align: center;
  }

  .content {
    padding: 20px;
    border: 1px solid #ddd;
  }
</style>

<div>
  <!-- Header section -->
  <div class="header">
    <h1>{title}</h1>
  </div>

  <!-- Additional content -->
  <!-- <div class="content">
    <p>{content}</p>
  </div> -->
</div>
