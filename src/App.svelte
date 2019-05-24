<script>
	let name = 'Attila';
	let age = 33;

	function incrementAge(){
		age += 1;
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name}, you are {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
