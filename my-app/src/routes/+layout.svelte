<script>
	import Navbar from './Navbar.svelte';
	import Footer from './Footer.svelte';
	import './styles.css';
</script>

<svelte:head>
  <title>Temples of India | Home</title>
</svelte:head>
<div class="app">
	<Navbar />

	<main>
		<slot />
	</main>

	<Footer/>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
		background-color: white;
		padding:10px;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}


</style>
