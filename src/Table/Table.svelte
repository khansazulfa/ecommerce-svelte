<script >
  import { Button, Table } from 'sveltestrap';
  import { onMount } from 'svelte';
  onMount(() => {
		let t = document.getElementById('table');
		console.log(t.textContent);
	});
  
</script>

<Table bordered id="table">
  <thead>
    <tr>
      <th>ID</th>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Username</th>
      <th>Aksi</th>
    </tr>
  </thead>
  <tbody>
  <tr>
       <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
      <td><Button>Ubah Data </Button></td>  
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
      <td><Button>Ubah Data </Button></td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>Larry</td>
      <td>the Bird</td>
      <td>@twitter</td>
      <td><Button>Ubah Data </Button></td>
    </tr> 
  </tbody>
</Table>