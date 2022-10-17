<script>
  import '../global.css';
  import './sidebar.css';

  import { goto } from '$app/navigation';

  function gotoDashboard() {
    goto('/dashboard');
  }
  function gotoDataUser() {
    goto('/datauser');
  }
  function gotoDataPemesanan() {
    goto('/datapemesanan');
  }
  function gotoDataLayanan() {
    goto('/datalayanan');
  }

  function active() {
    const background = orange;
    return;
  }
</script>

<div class="sidebar-field">
  <div class="dashboard-link" on:click={gotoDashboard}>
    <i class="uil uil-dashboard" />
    <span>Beranda</span>
  </div>
  <div class="datauser-link" on:click={gotoDataUser}>
    <i class="uil uil-user-plus" />
    <span>Data User</span>
  </div>
  <div class="datapemesanan-link" on:click={gotoDataPemesanan}>
    <i class="uil uil-shopping-cart-alt" />
    <span>Data Pemesanan</span>
  </div>
  <div class="datalayanan-link" on:click={gotoDataLayanan}>
    <i class="uil uil-heart-medical" />
    <span>Data Layanan</span>
  </div>
</div>
