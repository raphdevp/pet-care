<script>
  import Sidebar from '../../lib/components/sidebar/sidebar.svelte';
  import Navbar from '../../lib/components/navbar/navbar.svelte';

  import './dashboard.css';
</script>

<title>Dashboard</title>
<div class="dashboard-continer">
  <div class="navbar">
    <Navbar />
  </div>
  <div class="main-content">
    <Sidebar />
    <div class="card">
      <h1>Beranda</h1>
      <div class="card-border">
        <div class="content-card">
          <div class="main-card">
            <h2>Data User</h2>
            <span>0</span>
          </div>
        </div>
        <div class="content-card">
          <div class="main-card">
            <h2>Data Pemesanan</h2>
            <span>0</span>
          </div>
        </div>
      </div>
      <div class="card-border">
        <div class="content-card">
          <div class="main-card">
            <h2>Data Layanan</h2>
            <span>0</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
