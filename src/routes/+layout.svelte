<script lang="ts">
	import { Svrollbar } from 'svrollbar';
	import '../app.css';
	import GitHub from '$lib/icons/git-hub.svelte';
	import LinkedIn from '$lib/icons/linked-in.svelte';
	import Instagram from '$lib/icons/instagram.svelte';
	import Amazon from '$lib/icons/amazon.svelte';
</script>

<main>
	<slot />
</main>
<footer class="bg-slate-900 py-60 pt-10">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<a
			href="#top"
			class="mb-2 block text-xl font-bold text-slate-200 font-['Roboto_Mono']">
			RICHARD TAMMAR
		</a>
		<div
			class="flex justify-between border-t border-slate-800 pt-4 text-sm text-slate-300 sm:gap-32">
			<div>
				&copy; Richard Tammar 2025. My thanks to <a
					href="https://mario.tiscareno.dev"
					class="underline">
					Mario Tiscareno
				</a>
				 for the template.
			</div>
			<div class="flex">
				<a
					href="https://www.amazon.com/gp/product/1442138882?ie=UTF8&tag=themarsho-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=1442138882"
					class="mr-1 block h-8 w-8 p-1">
					<Amazon />
				</a>

				<a
					href="https://www.instagram.com/venusiancat/?hl=en"
					class="mr-1 block h-8 w-8 p-1">
					<Instagram />
				</a>

				<a
					href="https://github.com/VenusianCat"
					class="-ml-1 -mt-1 block h-10 w-10 p-1">
					<GitHub />
				</a>

				<a
					href="https://www.linkedin.com/in/richardtammar/"
					class="-mr-1 -mt-1 block h-10 w-10 p-1">
					<LinkedIn />
				</a>
			</div>
		</div>
	</div>
</footer>

<style lang="postcss">
	:global(html::-webkit-scrollbar, body::-webkit-scrollbar) {
		/* hide scrollbar */
		display: none;
	}

	:global(.v-scrollbar) {
		z-index: 100;
	}

	:global(.tooltip) {
		visibility: hidden;
		position: absolute;
	}

	:global(.tech-icon:hover .tooltip) {
		visibility: visible;
		z-index: 100;
	}

	@media (max-width: 768px) {
		:global(.v-scrollbar) {
			display: none;
		}
	}
</style>
