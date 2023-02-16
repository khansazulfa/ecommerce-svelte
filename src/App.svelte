<script>
  import Navbar from "./Navbar/Navbar.svelte";
  import Table from "./Table/Table.svelte";
  import TambahKeranjang from "./TambahKeranjang/TambahKeranjang.svelte";
  import { Container, ListGroup } from 'sveltestrap';
  import List from "./List/List.svelte";

</script>

<Navbar/>
<br>
<Container>
  
<Table/> 
<!-- <ListGroup>
  <List produk = {'Nivea'} desc = {'Hand Body'}/>
  <List produk = {'Vaseline'}/>
  <List/>
  <List/> 
</ListGroup> -->
<TambahKeranjang/>
</Container>
<style>
	
	@media (min-width: 640px) {
		
	}
</style>