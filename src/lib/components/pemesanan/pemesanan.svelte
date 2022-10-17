<script>
  import '../global.css';

  export let item = {};

  async function hapus(id) {
    const url = `http://localhost:8080/api/layanan${id}`;
    const response = await fetch(url, {
      method: 'DELETE',
      headers: {
        Accept: 'application/json',
        'Content-Type': 'application/json',
      },
    });

    const data = await response.json();

    if (response.status == 200) {
      console.log(response.status);
      alert(`${data.message}`);
    } else {
      console.log(response.status);
      alert(`${data.message}`);
    }
  }

  export let item2 = {};

  async function edit(id) {
    const url = `http://localhost:8080/api/layanan${id}`;
    const response = await fetch(url, {
      method: 'DELETE',
      headers: {
        Accept: 'application/json',
        'Content-Type': 'application/json',
      },
    });

    const data = await response.json();

    if (response.status == 200) {
      console.log(response.status);
      alert(`${data.message}`);
    } else {
      console.log(response.status);
      alert(`${data.message}`);
    }
  }
</script>

<tr>
  <td />
  <td />
  <td />
  <td />
  <td />
  <td />
  <td />
  <td>
    <a href="/datauser" target="_self" on:click={() => edit(item2.id)}>
      <i class="uil uil-edit" />
    </a>
    <a href="/datapemesanan" target="_self" on:click={() => hapus(item.id)}>
      <i class="uil uil-trash-alt" />
    </a>
  </td>
</tr>
