<script>
    import { Col, Container, Row, Button } from 'sveltestrap';

    let keranjang = 0
	let harga = 1000000

	$: hargaTotal = keranjang * harga


	function tambahKeranjang () {
		keranjang +=1
	}   
</script>

<Container>
	<br>
<Row>
	<Col><Button on:click={tambahKeranjang}> Add to chart</Button></Col>
	<Col>Jumlah Barang {keranjang} <br> Harga Total : Rp {hargaTotal}</Col>
</Row>
</Container>