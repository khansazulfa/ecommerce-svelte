<script >
	
  import { Button, Table } from 'sveltestrap';
  import { onMount } from 'svelte';

  onMount(() => {
    let t = document.getElementById('table');
    console.log(t.textContent);
  });
  
  let user =[
    {
      id:'0001',
      firstname: 'Mark',
      lastname: 'Lee',
      username: '@mddow'
    },
     {
      id:'0002',
      firstname: 'Dern',
      lastname: 'Wuu',
      username: '@drrn'
    }, {
      id:'0001',
      firstname: 'Joe',
      lastname: 'Nas',
      username: '@jjns'
    }
  ]

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
    {#each user as u, i } 
      <tr>
        <th scope="row">{i + 1}</th>
        <td>{u.firstname}</td>
        <td>{u.lastname}</td>
        <td>{u.username}</td>
        <td>
           <Button>Ubah Data</Button>
        </td>  
      </tr>
       {/each}
    </tbody>
  </Table>

  <style>

  </style>