<script>
  import Sidebar from '../../lib/components/sidebar/sidebar.svelte';
  import Navbar from '../../lib/components/navbar/navbar.svelte';
  import User from '../../lib/components/user/user.svelte';
  import '../../lib/components/global.css';
  import './datauser.css';
  export let data = {
    data: [],
  };
  console.log(data);
</script>

<title>Data User</title>
<div class="datapemesanan-continer">
  <div class="navbar">
    <Navbar />
  </div>
  <div class="main-content">
    <Sidebar />
    <div class="table-field">
      <h1>Data User</h1>
      <input class="search" type="search" placeholder="Search " />
      <table>
        <tr>
          <th>Id User</th>
          <th>Nama Lengkap</th>
          <th>Email</th>
          <th>Tindakan</th>
        </tr>
        <!-- {#each data.data as item}
          <User {item} />
        {/each} -->
        <User />
      </table>
    </div>
  </div>
</div>

<style>
  .search {
    margin-left: 758px;
    width: 200px;
    text-align: end;
    border: 2px solid black;
    border-radius: 12px;
    height: 30px;
  }
</style>
