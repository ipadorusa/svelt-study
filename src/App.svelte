<script>
	import List from './components/List.svelte';
	import Modal from './components/Modal/Modal.svelte';

	export let name;
	let showModal;
	let color = 'black';

	const handleClick = () => {
		color = 'blue'
	}
	const handleInput = (e) => {
		color = e.target.value;
	}
	const toggleModal = () => showModal = !showModal;


</script>

<main>
	<h1>Hello {name}!</h1>
	<p style='color:{color}'>{color} jean</p>
	<button type="button" on:click="{handleClick}">update jean color</button>
	<input type="text" bind:value={color}/>
	<button type="button" on:click={toggleModal}>open modal</button>
	<List />
	<Modal message='I am a prop value' {showModal} on:click={toggleModal} />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>