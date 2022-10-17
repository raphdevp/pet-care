<script>
  import Navbar from '../../lib/components/navbar/navbar.svelte';
  import Sidebar from '../../lib/components/sidebar/sidebar.svelte';
  import Layanan from '../../lib/components/layanan/layanan.svelte';
  import '../../lib/components/global.css';

  export let data = {
    data: [],
  };
  console.log(data);
</script>

<div class="datalayanan-continer">
  <div class="navbar">
    <Navbar />
  </div>
  <div class="main-content">
    <Sidebar />
    <div class="table-field">
      <h1>Data Layanan</h1>
      <a href="/datalayanan/create"><i class="uil uil-plus-circle" /></a>
      <table>
        <tr>
          <th>Judul Layanan</th>
          <th>Harga</th>
          <th>Gambar</th>
          <th>Status</th>
          <th>Tindakan</th>
        </tr>
        {#each data.data as item}
          <Layanan {item} />
        {/each}
        <!-- <Layanan /> -->
      </table>
    </div>
  </div>
</div>

<style>
  .datalayanan-continer {
    width: 100%;
    height: 100vh;
  }

  .datalayanan-continer .navbar {
    position: relative;
    height: 0;
    background: blue;
  }
  .datalayanan-continer .main-content {
    /* position: relative; */
    display: flex;
    flex-direction: row;
  }

  .main-content .table-field {
    background: #eeeeee;
    flex-grow: 1;
    display: flex;
    flex-direction: column;
  }

  .table-field h1 {
    margin: 120px 40px 0 40px;
    font-size: 42px;
    font-weight: 700;
    width: max-content;
    height: min-content;
  }
  .table-field a {
    text-decoration: none;
  }

  .table-field a i {
    display: flex;
    justify-content: flex-end;
    margin-right: 145px;
    font-size: 42px;
    color: black;
  }

  .table-field table {
    border-radius: 5px;
    font-size: 20px;
    font-weight: normal;
    border-collapse: collapse;
    white-space: nowrap;
    border: 2px solid black;
    background-color: white;
    margin: 20px 70px 70px 40px;
    box-shadow: 0px 35px 50px rgba(0, 0, 0, 0.3);
  }

  table th {
    color: #ffffff;
    background: #19749e;
  }
  table th {
    border: 1px solid black;
    height: 50px;
    text-align: center;
  }

  table th:nth-child(odd) {
    color: #ffffff;
    background: #324960;
  }
  table tr:nth-child(even) {
    background: #d9d9d9;
  }
</style>
