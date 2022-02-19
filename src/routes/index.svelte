<script context="module">
	export const prerender = true;
</script>

<script>
	import { fly } from 'svelte/transition';

	import FaBicycle from 'svelte-icons/fa/FaBicycle.svelte'
	import FaInstagram from 'svelte-icons/fa/FaInstagram.svelte'
	import TiMail from 'svelte-icons/ti/TiMail.svelte'

	import AutoGallery from '$lib/autogallery/AutoGallery.svelte'

	let images = [
		{
			'src': 'static/amwaffles.jpg',
			'alt': '',
		},
		{
			'src': '',
			'alt': '',
		},
	]
</script>


<svelte:head>
	<title>Holland's Profile Page</title>
</svelte:head>

<section id="main">
	<header>
		<h1 id="headline">
			Holland Wilson<br /><span class="subtitle">Chevalier de Cuisine</span>
		</h1>
		<img id="headshot" src="static/headshot.png" alt="A picture of me at Caroline's in Joplin.">
	</header>

	<article id="bio">
		<section id="contact">
			<h2>
				Contact Info
			</h2>
			
			<p class="address">
				<label for="insta" class="icon"><TiMail /></label> <a href="mailto:ChefHolland@eclectic-co.com">ChefHolland@eclectic-co.com</a>
			</p>
			<p class="address">
				<label for="insta" class="icon"><FaInstagram /></label> <a href="https://instagram.com/damned_scholar" id="insta" target="_blank" rel="noopener noreferrer">@damned_scholar</a>
			</p>
		</section>
	
		<section id="about">
			<h2>
				My Journey
			</h2>
	
			<p>Somehow, I've wound up transmuting a nerd with too many hobbies into a multi-niche foodservice and hospitality junkie. I've had the privilege to learn from some of Springfield, MO's finest restaurants and am in the habit of acquiring multiple new skills a year. I have developed and sold vegan cheese, tended multiple bars, manufactured high-quality desserts to exacting specifications, single-handedly catered events, and engaged in publicity events to promote my work community on Commercial Street.</p>
		</section>
	</article>

	<article id="cv">
		<h2>
			Looking for something special?
		</h2>

		<p>If you have a demanding event concept but don't want to put too much work into planning the food, a new foodservice concept that needs methodical R&D, a class that could benefit from a hands-on lecture about science topics, or similar projects, let's talk. I'm an experienced event chef and available as a freelance consultant.</p>
	</article>

	<!-- <section id="gallery">
		<AutoGallery />
	</section> -->
</section>

<style>
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
		color: var(--heading-color);
		margin: 5px;
	}
	h2 {
		font-size: 1.4rem;
		width: 100%;
		color: var(--heading-color);
		margin: 5px;
	}
	h3 {
		width: 100%;
		color: var(--heading-color);
		margin: 5px;
	}
	h4 {
		width: 100%;
		color: var(--heading-color);
		margin: 5px;
	}
	h5 {
		width: 100%;
		color: var(--heading-color);
		margin: 5px;
	}

	#main {
		background-color: #E6E2DB;
		box-shadow: 4px 5px 10px 5px rgba(154,126,76,0.55);
		border-radius: 8px;
		padding: 10px;
		margin-top: 120px;
	}

	#main header {
		display: flex;
		align-items: flex-end;
		height: 100px;
		width: 100%;
		overflow: visible;
	}

	#headline {
		display: inline-block;
	}
	#headshot {
		position: relative;
		bottom: -40px;
	}

	#bio {
		display: flex;
		align-items: flex-start;
	}

	.address {
		display: grid;
		grid-template-columns: 20px 270px;
		grid-template-rows: repeat(2, auto);
		grid-column-gap: 4px;
		grid-row-gap: 4px;
		margin-bottom: 0;
	}

	#about {
		flex-grow: 2;
	}

	.subtitle {
		font-size: 80%;
		font-style: italic;
	}

	.icon {
		width: 16px;
		height: 16px;
	}

</style>
