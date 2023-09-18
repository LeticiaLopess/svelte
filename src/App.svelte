<script>
	import ContactCard from "./ContactCard.svelte";

	export let name = 'Let';
	export let age = 22;

	function incrementAge() {
		age += 1;
	}

	// let uppercaseName; not required!

	$: uppercaseName = name.toUpperCase(); // we added a new variable "uppercaseName", but we don't need to declare it before use

	$: console.log(name) // whenever name changes it will rerun

	$: if (name === "Let") {
		age = 25
	}

	function changeName() {
		name = "Leticia";
	}

	function nameInput(event) {
		const enteredValue = event.target.value;
		name = enteredValue;
	}
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {name.toUpperCase()}, my age is {age}!</h1>
<button on:click="{incrementAge}">Change Age</button>
<!-- <button on:click="{changeName}">Change Name</button> -->

<!-- <input type="text" value="{name}" on:input={nameInput}> -->

<!-- by default, the data flow in svelte is unidirectional, which means here we're outputting data -->

<!-- we can use the shortcut bind instead of on:event to update the value -->

<input type="text" bind:value="{name}" on:input={nameInput}>
<!-- it will also and automatically change the name if it's changed -->

<ContactCard />