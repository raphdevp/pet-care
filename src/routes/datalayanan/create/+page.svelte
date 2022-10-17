<script>
  import Navbar from '../../../lib/components/navbar/navbar.svelte';
  import Sidebar from '../../../lib/components/sidebar/sidebar.svelte';
  import '../../../lib/components/global.css';

  function Create() {
    fetch('http://localhost:8080/api/layanan', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        id: '',
        name: '',
        image: 'req.body.image',
        service: [
          {
            name: '10:10',
            harga: '50',
          },
          {
            jam: '10:10',
            harga: '50',
          },
        ],
      }),
    }).then((p) => {
      p.json().then((v) => console.log(v));
    });
  }
</script>

<div class="datalayanan-continer">
  <div class="navbar">
    <Navbar />
  </div>
  <div class="main-content">
    <Sidebar />
    <div class="table-field">
      <h1>Data Layanan</h1>
      <form>
        <label for="Judul">Judul Layanan</label>
        <input class="inpt" type="text" />
        <label for="Harga">Harga</label>
        <input class="inpt" type="text" />
        <label for="Harga">Status</label>
        <input class="inpt" type="text" />
        <label class="inpt-img" for="Gambar">Gambar</label>
        <input type="file" required />
        <button on:click={async () => await Create()}>Submit</button>
      </form>
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
    /* border: 2px solid black; */
  }

  .table-field h1 {
    margin: 120px 40px 0 40px;
    font-size: 42px;
    font-weight: 700;
    width: max-content;
    height: min-content;
  }

  .table-field form {
    /* border: 2px solid black; */
    display: flex;
    flex-direction: column;
    margin-left: 40px;
  }

  .table-field form label {
    margin-top: 10px;
    font-size: 28px;
    font-weight: 700;
  }

  .table-field form .inpt {
    border-radius: 12px;
    width: 700px;
    height: 40px;
    box-shadow: 10px 10px 25px rgba(0, 0, 0, 0.2);
  }
  .table-field form button {
    background: orange;
    color: #eeeeee;
    font-weight: 700;
    border: none;
    width: 120px;
    height: 40px;
    border-radius: 5px;
    margin-left: 580px;
  }
</style>
