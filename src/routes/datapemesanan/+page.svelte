<script>
  import '../../lib/components/global.css';
  import Navbar from '../../lib/components/navbar/navbar.svelte';
  import Sidebar from '../../lib/components/sidebar/sidebar.svelte';
  import Pemesanan from '../../lib/components/pemesanan/pemesanan.svelte';
  import './datapemesanan.css';
</script>

<title>Data Pemesanan</title>
<div class="datapemesanan-continer">
  <div class="navbar">
    <Navbar />
  </div>
  <div class="main-content">
    <Sidebar />
    <div class="table-field">
      <h1>Data Pemesanan</h1>
      <input class="search" type="search" placeholder="Search " />
      <table>
        <tr>
          <th>Id Pesanan</th>
          <th>Nama Lengkap</th>
          <th>Nama Layanan</th>
          <th>Alamat</th>
          <th>Status</th>
          <th>Booking / Home Service</th>
          <th>Harga</th>
          <th>Hapus</th>
        </tr>
        <!-- {#each data.data as item}
          <Pemesanan {item} />
        {/each} -->
        <Pemesanan />
      </table>
    </div>
  </div>
</div>

<style>
  .search {
    margin-left: 760px;
    width: 200px;
    text-align: end;
    border: 2px solid black;
    border-radius: 12px;
    height: 30px;
  }
</style>
