<script>
	import Header from '../components/header/header.svelte';

	import '../font-face.css';
	import '../global.css';

	let { children } = $props();
</script>

<svelte:head>
	<!-- <link rel="icon" href={favicon} /> -->
</svelte:head>

<main>
	<Header />
	{@render children?.()}
</main>
