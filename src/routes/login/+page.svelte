<script>
  let email = '';
  let password = '';

  async function login() {
      const response = await fetch('/api/auth/login', {
          method: 'POST',
          headers: { 'Content-Type': 'application/json' },
          body: JSON.stringify({ email, password })
      });

      if (response.ok) {
          const data = await response.json();
          // Handle successful login
      } else {
          // Handle login error
      }
  }
</script>

<style>
  :global(html, body) {
      height: 100%;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
  }

  .container {
      background: white;
      padding: 2rem;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      max-width: 400px;
      width: 100%;
  }

  h1 {
      margin-bottom: 1.5rem;
      font-size: 1.5rem;
  }

  form {
      display: flex;
      flex-direction: column;
  }

  label {
      margin-bottom: 0.5rem;
      text-align: left;
      font-weight: bold;
  }

  input {
      padding: 0.5rem;
      margin-bottom: 1rem;
      border: 1px solid #ccc;
      border-radius: 4px;
      font-size: 1rem;
  }

  button {
      padding: 0.5rem;
      background-color: #007BFF;
      color: white;
      border: none;
      border-radius: 4px;
      font-size: 1rem;
      cursor: pointer;
      margin-top: 1rem;
  }

  button:hover {
      background-color: #0056b3;
  }

  footer {
      margin-top: 1rem;
      font-size: 0.9rem;
      color: #777;
  }

  footer a {
      color: #007BFF;
      text-decoration: none;
  }

  footer a:hover {
      text-decoration: underline;
  }
</style>

<div class="container">
  <header>
      <h1>Welcome Back</h1>
  </header>

  <main>
      <form on:submit|preventDefault={login}>
          <label for="email">Enter your email</label>
          <input type="email" id="email" bind:value={email} required />

          <label for="password">Enter your password</label>
          <input type="password" id="password" bind:value={password} required />

          <button type="submit">Login</button>
      </form>
  </main>

  <footer>
      <p>Don't have an account? <a href="/register">Register now</a></p>
  </footer>
</div>
