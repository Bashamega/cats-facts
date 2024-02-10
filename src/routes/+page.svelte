<script>
	let fact = '';
	function generate(){
		fetch('https://catfact.ninja/fact')
		.then(res=>res.json())
		.then(data=>{
			fact = data.fact;
		})
	}
	generate()
</script>
<section>
	<h1>Cat facts generator</h1>
	<button on:click={generate}>Regenerate</button>
	<p>Did you know that</p>
	<div id="fact">{fact}</div>
</section>
