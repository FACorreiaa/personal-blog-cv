<script>
	import '../app.css';

	import Header from '../lib/Header.svelte';
	import Footer from '../lib/Footer.svelte';
</script>

<header>
	<Header />
</header>

<main class="bg-purple-200">
	<slot />
</main>

<footer>
	<Footer />
</footer>

<style>
	main {
		flex: 1;
		padding: 15px;
		overflow-y: auto;
	}
</style>
