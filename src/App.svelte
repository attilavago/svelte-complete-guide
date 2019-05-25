<script>
	import ContactCard from './ContactCard.svelte';

	let name = 'Atti';
	let age = 33;
	let jobTitle = '';
	let image = '';
	let description = '';

	$: upperCaseName = name.toUpperCase();

	function incrementAge(){
		age += 1;
	}

	function changeName(){
		name = 'Attila';
	}

	function nameInput(event){
		const enteredValue  = event.target.value;
		name = enteredValue;
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {upperCaseName}, you are {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<!-- <button on:click={changeName}>Change Name</button> -->
<!-- <input type="text" value="{name}" on:input={nameInput}> -->
<input type="text" value="{name}" bind:value={name}>
<input type="text" value="{jobTitle}" bind:value={jobTitle}>
<input type="text" value="{image}" bind:value={image}>
<textarea rows="3" value="{description}" bind:value={description}></textarea>


<ContactCard 
	userName={name} 
	{jobTitle} 
	{description} 
	userImg={image}
/>

