<script context="module">
	export const prerender = true;
</script>

<script>
	import { fly } from 'svelte/transition';

	import FaBicycle from 'svelte-icons/fa/FaBicycle.svelte'
	import FaInstagram from 'svelte-icons/fa/FaInstagram.svelte'

	import Gallery from 'svelte-gallery';

	const images = [
		{ src: 'https://source.unsplash.com/random', width: 600, height: 400 },
		{ src: 'https://source.unsplash.com/random', width: 400, height: 600 },
		{ src: 'https://source.unsplash.com/random', width: 800, height: 1200 },
		{ src: 'https://source.unsplash.com/random', width: 300, height: 200 },
	];
</script>


<svelte:head>
	<title>Holland's Profile Page</title>
</svelte:head>

<section id="main">
	<h1>
		Holland Wilson, Chevalier de Cuisine
	</h1>

	<section id="contact">
		<h2>
			Contact Info
		</h2>
		
		<label for="insta"><FaInstagram /></label> <a href="https://instagram.com/damnedscholar" target="_blank" rel="noopener noreferrer">@damnedscholar</a>
	</section>

	<section id="about">
		<h2>
			My Journey
		</h2>

		<p>Somehow, I've wound up transmuting a nerd with too many hobbies into a multi-niche foodservice and hospitality junkie. I've had the privilege to learn from some of Springfield, MO's finest restaurants and am in the habit of acquiring multiple new skills a year. I have developed and sold vegan cheese, tended multiple bars, manufactured high-quality desserts to exacting specifications, single-handedly catered events, and engaged in publicity events to promote my work community on Commercial Street.</p>
	</section>

	<section id="gallery">
		<Gallery {images} />
	</section>
</section>

<style>
	:root {
		--text: #06254B;
		--text-accent: #27235D;
		--text-head: #0F0B50;
		--frame-bg: #1D3957;
		--content-bg: #CFC5B4;
		--content-border-inner: #9A7E4C;
		--content-border-outer: #734B00;
	}
	body {
		background-color: var(--bg-frame);
	}
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
		z-index: 1;
	}

	h1 {
		width: 100%;
		color: var(--text-head)
	}
	h2 {
		width: 100%;
		color: var(--text-head)
	}
	h3 {
		width: 100%;
		color: var(--text-head)
	}
	h4 {
		width: 100%;
		color: var(--text-head)
	}
	h5 {
		width: 100%;
		color: var(--text-head)
	}

	#main {
		background-color: #E4D6A8;
	}

</style>
