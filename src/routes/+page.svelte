<script lang="ts">
	let heroText = $state('');
	let heroTextList: string[] = ['Shopify Development', 'E-commerce Solutions', 'Custom Storefronts', 'App Integrations'];

	const heroTextAnimation = async (textList: string[]) => {
		const delay = (ms: number) => new Promise((resolve) => setTimeout(resolve, ms));

		while (true) {
			for (let heroLine of textList) {
				for (let i = 0; i <= heroLine.length; i++) {
					heroText = heroLine.substring(0, i + 1);
					await delay(100);
				}
				for (let i = heroLine.length; i >= 0; i--) {
					heroText = heroLine.substring(i, 0);
					await delay(50);
				}
				await delay(1000);
			}
		}
	};
	heroTextAnimation(heroTextList);
</script>

<div id="main">
	<section id="hero">
		<div class="grid grid-cols-3 place-content-center h-full">
			<span class="flex items-center justify-center"><img src="/BM.png" alt="blue maple logo" class="h-1/2" /></span>
			<div class="col-span-2 flex items-center font-mono text-5xl">{heroText} <span class="blinking">_</span></div>
		</div>
	</section>
	<section id="about">
		<h2>Here to elevate your customer's shopify experience</h2>
	</section>
	<section id="tech"></section>
	<section id="showcase"></section>
	<section id="contact">Contact Us for a free quote</section>
</div>

<style>
	#main {
		background-color: black;
	}
	#hero {
		height: 100vh;
		color: rgb(0, 200, 255);
	}
	.blinking {
		animation: blinker 1.5s step-end infinite;
	}
	@keyframes blinker {
		50% {
			opacity: 0;
		}
	}
</style>
