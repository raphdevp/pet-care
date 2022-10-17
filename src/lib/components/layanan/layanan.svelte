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
  // import { load } from "../../../routes/coba/+page.js";
</script>

<tr>
  <td />
  <td />
  <td />
  <td />
  <td>
    <i class="uil uil-edit" />
    <i class="uil uil-edit" />
  </td>
  <td>
    <a href="/datalayanan" target="_self" on:click={() => hapus(item.id)}>
      <i class="uil uil-trash-alt" />
    </a>
  </td>
</tr>
<!-- <tr>
  <td>
    {item}
  </td>
  <td>
    {item}
  </td>
  <td>
    <i class="uil uil-edit" />
  </td>
  <td>
    <a href="/datalayanan" target="_self" on:click={() => hapus(item.id)}>
      <i class="uil uil-trash-alt" />
    </a>
  </td>
</tr> -->

<!-- <tr>
  <td>
    {item.id}
  </td>
  <td>{item.name}</td>
  <td>
    <i class="uil uil-edit" />
  </td>
  <td>
    <i class="uil uil-trash-alt" />
  </td>
</tr> -->
<style>
  td {
    border: 1px solid black;
    height: 50%;
    text-align: center;
  }
  td i {
    font-size: 32px;
  }
</style>
