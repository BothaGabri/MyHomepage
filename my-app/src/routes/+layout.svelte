<script>
	import favicon from "$lib/assets/favicon.svg";

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<title>Angel Software - Your Dev Partner</title>
</svelte:head>

<!-- Top Border -->
<div class="border top"></div>


<nav>
  <a href="/">Home</a>
  <a href="/services">Services</a>
</nav>
<!-- Header -->
<header>
	<img src="/images/API logo.png" alt="Angel Software Logo" />
</header>

{@render children()}

<style>
	/* Header */
	header {
		text-align: center;
		margin-bottom: 20px;
		border-bottom: 1.5px solid #444;
		width: 100%;
		padding-bottom: 20px;
	}
	header img {
		max-width: 100%;
		height: auto;
	}

</style>