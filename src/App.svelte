<script>
	// import Greeting from "./components/greetings.svelte";
	// export let name;
	// let data = "Any data"

	// let a = 0;

	// function updateNum() {
	// 	a = 24;
	// };
	// let firstName = 'John';
	// let lastName = 'Doe';

	// $: fullName = `${firstName} ${lastName}`
	// console.log("fullName", fullName)

		let count = 0;
		function increment() {
			count += 1;
		}

		let flowers = ['Jasmin', 'Hibiscus', 'Tulip'];
</script>

<main>
	<!-- <Greeting data = "Good evening"/>
	<h1>Hello {name}!</h1> -->
	
	<!-- <p>My First name is {firstName}</p>
	<p>My Last name is {lastName}</p>
	<button on:click={ () => {firstName = "Varsha" ; lastName = "Zurange"}}> Update Name</button>
	<p>{fullName}</p> -->

	<button on:click={increment}>
		Clicked {count}
	</button>

	<p>{count}</p>
	{#if count > 7}
		<p>{count} is greater than 7</p>

	{:else if count < 5}
		<p>{count} is less than 5</p>

	{:else}
		<p>{count} is between 5 to 7</p>
	{/if}
	
	<p>Flowers are: </p>
	{#each flowers as flower}
		<h3>{flower}</h3>
	{/each}

	<!-- <p>{a}</p> -->
	<!-- <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p> -->
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	/* h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	} */

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>