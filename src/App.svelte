<script>
	let name = 'Atti';
	let age = 33;

	$: upperCaseName = name.toUpperCase();

	function incrementAge(){
		age += 1;
	}

	function changeName(){
		name = 'Attila';
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {upperCaseName}, you are {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<button on:click={changeName}>Change Name</button>
