<script>
	import { Col, Container, Row, Button } from 'sveltestrap';
	
	let keranjang  = 0
	let harga = 100000

	$: hargatotal = keranjang * harga

	function tambahKeranjang(){
		keranjang +=1
	}

	let box = 'blue'
	function setcolor(){
		box=='blue'?box='red':box='blue'
	}
</script>

<Container>
	<Row>
	<Col>
		<br>
		<Button on:click={tambahKeranjang}>Add to chart</Button>
	</Col>
	<Col>
		<br>
		Jumlah Keranjang: {keranjang} <br> 
		Harga Total: Rp {hargatotal}</Col>
	<Col>
	<br>
	<button on:click={setcolor}>Change color</button>
	{#if box=='red'}
	<h2 style="background-color:orangered ;"> Iam Orangered</h2>
		{:else}
		<h2 style="background-color: blue ;">Iam Blue</h2>
	{/if}
	</Col>
	</Row>
</Container>