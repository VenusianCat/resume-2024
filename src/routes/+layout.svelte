<script lang="ts">
	import { Svrollbar } from 'svrollbar';
	import '../app.css';
	import GitHub from '$lib/icons/git-hub.svelte';
	import LinkedIn from '$lib/icons/linked-in.svelte';
</script>

<Svrollbar />

<main>
	<slot />
</main>
<footer
	class="left-0 -mt-2 w-full overflow-hidden bg-gradient-to-b from-slate-900 to-slate-900 py-12">
	<div class="relative mx-auto max-w-7xl px-4 md:px-6">
		<a
			href="#top"
			class="mb-2 block text-base font-bold tracking-tight text-slate-400">
			RICHARD TAMMAR
		</a>
		<ul
			class="flex justify-between border-t border-slate-800 pt-8 text-sm text-slate-500 sm:gap-32">
			<li class="hidden flex-1 sm:block"></li>
			<li>
				<ol
					class="flex flex-col gap-2 font-medium leading-loose tracking-tight">
					<!--<li><a href="#about">ABOUT ME</a></li>
					<li><a href="#skills">SKILLS</a></li>-->
					<li><a href="#work">EXPERIENCE</a></li>
					<li><a href="#education">EDUCATION</a></li>
				</ol>
			</li>
			<li class="flex">
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
