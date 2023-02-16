<script>
	import { Col, Container, Row, Button } from 'sveltestrap';
	
	let box = 'blue'
	function setcolor(){
		box=='blue'?box='red':box='blue'
	}
</script>

<Container>
	<br>
	<button on:click={setcolor}>Change color</button>
	{#if box=='red'}
	<h2 style="background-color:orangered ;"> Iam Orangered</h2>
		{:else}
		<h2 style="background-color: blue ;">Iam Blue</h2>
	{/if}
</Container>