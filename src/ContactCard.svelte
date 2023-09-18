<script>
</script>

<div class="contact-card">
  <header>
    <div class="thumb">
      <img src="" alt="" />
    </div>
    <div class="user-data">
      <h1>User Name</h1>
      <!-- if I have an h1 at App.svelte, and there we have an h1 style, both will merge with this style -->
      <h2>Job Title</h2>
    </div>
  </header>
  <div class="description">
    <p>A short description</p>
  </div>
</div>

<style>
  .contact-card {
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
    max-width: 30rem;
    border-radius: 5px;
    margin: 1rem 0;
  }

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .thumb {
    width: 33%;
    height: 100%;
  }

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .user-data {
    width: 67%;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  h1 {
    font-size: 1.25rem;
    font-family: "Roboto Slab", sans-serif;
  }

  h2 {
    font-size: 1rem;
    font-weight: normal;
    color: #5a5a5a;
  }

  .description {
    border-top: 1px solid #ccc;
    padding: 1rem;
  }
</style>
