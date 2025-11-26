<script lang="ts">
	let heroText = $state('Shopify Development');
	let heroTextList: string[] = ['Shopify Development', 'E-commerce Solutions', 'Custom Storefronts', 'App Integrations'];

	const heroTextAnimation = (textList: string[]) => {
		let index = 0;
		let subStringIndex = 0;
		setInterval(() => {
			heroText = textList[index].substring(0, subStringIndex + 1);
			subStringIndex++;
			if (subStringIndex > textList[index].length) {
				subStringIndex = 0;
			}
			if (subStringIndex === 0) {
				index = (index + 1) % textList.length;
			}
		}, 100);
	};
	// heroTextAnimation(heroTextList);
</script>

<section id="hero">
	<div class="grid grid-cols-3 place-content-center h-full">
		<span class="flex items-center justify-center"><img src="/BM.png" alt="blue maple logo" class="h-1/2" /></span>
		<div class="col-span-2 flex items-center font-mono text-4xl">{heroText} <span class="blinking">_</span></div>
	</div>
</section>
<section id="tech"></section>
<section id="showcase"></section>

<style>
	#hero {
		height: 100vh;
		background-color: black;
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
