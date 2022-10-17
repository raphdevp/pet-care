<script>
  import './navbar.css';
  import '../global.css';
  import { goto } from '$app/navigation';
  function signOut() {
    goto('/');
  }
</script>

<nav>
  <div class="logo">
    <h1>Pet Care</h1>
  </div>

  <i on:click={signOut} class="uil uil-signout" />
</nav>
