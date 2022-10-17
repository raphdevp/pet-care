<script>
  import '../global.css';
  import './login.css';
  import { goto } from '$app/navigation';

  let email = 'eve.holt@reqres.in',
    password = 'cityslicka';

  async function login() {
    if (email == '' && password == '') {
      alert('`${data.message}`');
      return;
    }

    console.log(
      JSON.stringify({
        email,
        password,
      })
    );
    const url = 'https://reqres.in/api/login';
    const response = await fetch(url, {
      method: 'POST',
      headers: {
        Accept: 'application/json',
        'Content-Type': 'application/json',
      },
      body: JSON.stringify({
        email,
        password,
      }),
    });

    console.log(response.status);

    if (response.status == 200) {
      await goto('/dashboard');
    } else {
      const data = await response.json();
      console.log(response.status);
      alert(`${data.message}`);
    }
  }
</script>

<title>Pet Care</title>
<div class="continer">
  <div class="forms-login">
    <span>Login</span>
    <div class="input-form">
      <form on:submit|preventDefault={login}>
        <label for="Email">Email Address</label>
        <input bind:value={email} type="text" placeholder="Enter your email address" required />
        <i class="uil uil-envelope" />

        <label for="Password">Password</label>
        <input bind:value={password} type="text" placeholder="Enter your password" required />
        <i class="uil uil-lock" />

        <div class="button-field">
          <button type="submit">Login</button>
        </div>
      </form>
    </div>
  </div>
</div>
