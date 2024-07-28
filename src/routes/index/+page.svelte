<script>
  // Index page script (if needed)
</script>

<style>
  .page-container {
      display: flex;
      flex-direction: column;
      min-height: 100vh; /* Ensure it takes up the full viewport height */
      margin: 0;
      font-family: Arial, sans-serif;
      background: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSNaY7GLNVy1E7XTgXArRM86Dxbw6P1sh9yrg&s') no-repeat center center fixed; /* External background image */
      background-size: cover; /* Cover the entire viewport */
  }

  header {
      background: rgba(255, 255, 255, 0.8); /* Semi-transparent background */
      padding: 1rem;
      border-bottom: 1px solid #ddd;
      text-align: center;
  }

  footer {
      background: rgba(255, 255, 255, 0.8); /* Semi-transparent background */
      padding: 1rem;
      border-top: 1px solid #ddd;
      text-align: center;
      margin-top: auto; /* Pushes footer to the bottom */
  }

  .main-content {
      flex: 1; /* Takes up remaining space */
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 2rem;
  }

  .container {
      background: white;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      max-width: 90vw; /* Responsive max-width */
      width: 100%;
      box-sizing: border-box; /* Include padding in width calculation */
  }

  h1 {
      margin-bottom: 1.5rem;
      font-size: 2rem;
  }

  nav a {
      display: block;
      margin: 1rem 0;
      font-size: 1.2rem;
      text-decoration: none;
      color: #007BFF;
  }

  nav a:hover {
      text-decoration: underline;
  }

  footer p {
      margin: 0;
      font-size: 0.9rem;
      color: #777;
  }
</style>

<div class="page-container">
  <header>
      <h1>Welcome to the Real Estate Token Platform</h1>
  </header>

  <main class="main-content">
      <div class="container">
          <nav>
              <a href="/login">Login</a>
              <a href="/register">Register</a>
          </nav>
      </div>
  </main>

  <footer>
      <p>&copy; 2024 Real Estate Token Platform</p>
  </footer>
</div>
