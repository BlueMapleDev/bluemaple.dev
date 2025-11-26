<script lang="ts">
	interface Props {
		title?: string;
		link?: string;
		image?: string;
		children?: import('svelte').Snippet;
	}

	let {
		title = 'Project Title',
		link = 'carsonwhite.dev',
		image = '/project_images/placeholder.png',
		children
	}: Props = $props();
</script>

<section class="grid sm:grid-cols-2 rounded-lg">
	<div class="grid grid-cols-4">
		<img
			class=" rounded-sm object-contain w-full h-full max-h-64"
			src={image}
			alt="website screenshot"
		/>
		<div class="col-span-3">
			<h2 class="text-2xl font-bold px-2 text-center">{title}</h2>
			<div class="mx-4">
				{@render children?.()}
			</div>
			<a class="underline text-blue-600" href="https://{link}">Visit Site</a>
		</div>
	</div>
</section>
