<script>
  import Navbar from "./Navbar/Navbar.svelte";
  import Table from "./Table/Table.svelte";
  import TambahKeranjang from "./TambahKeranjang/TambahKeranjang.svelte";
  import { Col, Container, Row } from 'sveltestrap';

</script>

<Navbar/>
<br>
<Container>
<Table/> 
<TambahKeranjang/>
</Container>
<style>
	
	@media (min-width: 640px) {
		
	}
</style>