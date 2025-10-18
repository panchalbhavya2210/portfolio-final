<script>
	import Header from '../components/header/header.svelte';
	// import favicon from '/favicon.svg';
	import '../font-face.css';
	import '../global.css';

	let { children } = $props();
</script>

<svelte:head>
	<title>Bhavya Panchal - Frontend Web Developer</title>
	<!-- <link rel="icon" href={favicon} /> -->
</svelte:head>

<main>
	<Header />
	{@render children?.()}
</main>
