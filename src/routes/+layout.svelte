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
<footer
	class="bg-slate-900 py-8">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<a
			href="#top"
			class="mb-2 block text-base font-bold tracking-tight text-slate-400">
			RICHARD TAMMAR
		</a>
		<ul
			class="flex justify-end border-t border-slate-800 pt-8 text-sm text-slate-500 sm:gap-32">
			<li class="flex">
				<a
					href="https://www.amazon.com/gp/product/1442138882?ie=UTF8&tag=themarsho-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=1442138882"
					class="block h-8 w-8 p-1 mr-1">
					<Amazon />
				</a>

				<a
					href="https://www.instagram.com/venusiancat/?hl=en"
					class="block h-8 w-8 p-1 mr-1">
					<Instagram />
				</a>

				<a
					href="https://github.com/VenusianCat"
					class="-ml-1 -mt-1 block h-10 w-10 p-1">
					<GitHub />
				</a>

				<a
					href="https://www.linkedin.com/in/richard-tammar/"
					class="-mr-1 -mt-1 block h-10 w-10 p-1">
					<LinkedIn />
				</a>
			</li>
		</ul>
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
