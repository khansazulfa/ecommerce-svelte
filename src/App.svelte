<script>
  import Navbar from "./Navbar/Navbar.svelte";
  import Table from "./Table/Table.svelte";
  import TambahKeranjang from "./TambahKeranjang/TambahKeranjang.svelte";
  import { Container, ListGroup } from 'sveltestrap';
  import List from "./List/List.svelte";

  let judul = "Tabel"

</script>

<Navbar/>
<br>
<Container>
  <!--Bind-->
  <p>{judul}</p>
  <input type="text" class="input mb-1" bind:value={judul} placeholder="Tulis disini"/>
  <button class="button">Enter</button>
  <Table/> 
<!-- Nampilin Props -->
<ListGroup>
  <List produk = {'Nivea'} desc = {'Hand Body'}/>
  <List produk = {'Vaseline'} desc = {'Hand Body'}/>
  <List produk = {'Avoskin'} desc = {'Hand Cream'}/>
  <List produk = {'Skingame'} desc = {'Moisturaizer'}/> 
</ListGroup> 
<TambahKeranjang/>
</Container>
<style>
	
	@media (min-width: 640px) {
		
	}
</style>