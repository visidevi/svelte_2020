<script>
	import About from './components/About.svelte'
	import Text from './components/Text.svelte'
	import Person from './components/Person.svelte'
	import Skills from './components/Skills.svelte'
	import Input from './components/Input.svelte'
	import Photos from './components/Photos.svelte'
	import ButtonCount from './components/ButtonCount.svelte'

	export let name;
	export let lastname;
	let sveletLogo='https://static.platzi.com/media/avatars/visaka-devi_ea7e8b70-a52b-466b-9fe9-d5d0cb405479'

	const data = {
		name: 'visaka',
		lastname: 'Devi',
		age: 27
	}

</script>


<style>

	:global(body) {
		background-color: #f2eee2;
		color: #0084f6;
	}
	:global(:root) {
		--theme-color: purple;
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	}

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



<main>
	<h1> {name} {lastname}!</h1>
	<p class="title">Front</p>
	<About/>
	<ButtonCount />
	<Input />
	<Text anotherText="Holi a todes"/>
	<Person data={data}/>
	<Person {...data} />
	<Skills />
	<Photos />
	<img src={sveletLogo} alt="">

</main>