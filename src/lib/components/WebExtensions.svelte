<script lang="ts">
	let extensions = [
		{
			title: 'RecurAlert',
			description:
				'Set recurring desktop notifications so you remember to regularly standup, drink water, breathe',
			link: 'https://addons.mozilla.org/en-US/firefox/addon/recuralert/',
			tech: 'Svelte, Tailwind'
		},
		{
			title: 'CaptchaLock',
			description:
				'No one likes captchas, make yourself solve one to stop yourself from mindlessly opening time-wasting websites',
			link: 'https://addons.mozilla.org/en-US/firefox/addon/captchaLock/',
			tech: 'Svelte, Tailwind'
		}
	];
</script>

<div class="">
	<div class=" mb-6">
		<h2 class="text-4xl pb-2 text-center md:text-left">Firefox Extensions</h2>
		<h3 class="text-2xl md:indent-4 text-center md:text-left">
			Utilities with minimalistic UIs, made with Svelte and TailwindCSS
		</h3>
	</div>
	{#each extensions as extension}
		<section class="grid md:grid-cols-4 ml-8 mb-4">
			<a href={extension.link} target="_blank">
				<h4 class="text-2xl underline text-blue-500">{extension.title}</h4>
			</a>
			<div class="text-lg col-span-3">
				<p>{extension.description}</p>
				<!-- <p>Made with {extension.tech}</p> -->
			</div>
		</section>
	{/each}
</div>
