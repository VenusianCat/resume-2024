<script>
	import LinkedIn from '$lib/icons/linked-in.svelte';
</script>

<div
	class="relative flex h-[60vh] w-full flex-col justify-start overflow-hidden bg-cover bg-right bg-no-repeat px-4"
	style="background-image: url('/images/headshot-2.jpg');">

	<ul class="flex items-end justify-between text-slate-700">
		<li class="block text-3xl font-bold tracking-tight">
			Hello World!
		</li>
		<li class="flex-1"></li>
		<li class="self-start">
			<a
				href="https://www.linkedin.com/in/richard-tammar/"
				class="-mr-1 block h-12 w-12 p-1">
				<LinkedIn />
			</a>
		</li>
	</ul>

	<div class="text-left text-2xl">
		<p class="block text-3xl font-bold tracking-tight">
			I'm Richard Tammar
		</p>
		<p
			class="mt-0 max-w-[30rem] pt-0 text-sm leading-snug tracking-tight text-slate-700 md:text-base [@media(min-height:600px)]:block">
			Affable, senior technologist with an aptitude for connecting the C-suite
			to the engine room. <!--Curious and analytical, I thrive anywhere I have the opportunity to
			catalyze positive change.-->
		</p>
		<!--mock code block-->
		<p
			class="mt-12 font-['Roboto_Mono'] font-medium leading-none tracking-tight text-[#df625d]/50 drop-shadow">
			<span class="font-normal text-slate-500/15">1</span>
			&nbsp;&nbsp;&lbrace;
		</p>
		<!--<p
			class="font-['Roboto_Mono'] font-medium leading-none tracking-tight text-slate-500 drop-shadow">
			<span class="font-normal text-slate-500/15">2</span>
			&nbsp;&nbsp;&nbsp;&nbsp;name: "Richard Tammar"<span class="text-indigo-500/50">,</span>
		</p>-->
		<p
			class="font-['Roboto_Mono'] font-medium leading-none tracking-tight text-slate-600 drop-shadow">
			<span class="font-normal text-slate-500/15">2</span>
			&nbsp;&nbsp;&nbsp;&nbsp;
			<span class="text-slate-500">message:</span>
			"Hello World!"
		</p>

		<p
			class="font-['Roboto_Mono'] font-medium leading-none tracking-tight text-[#df625d]/50 drop-shadow">
			<span class="font-normal text-slate-500/15">3</span>
			&nbsp;&nbsp;&rbrace;
			<!--<span
				class="cursor active font-['Roboto_Mono'] text-slate-500/30"
				id="cursor-1">
				&#x2590;
			</span>--><!--removed flashing cursor during development-->
		</p>
	</div>
	<div
		class="absolute bottom-12 left-0 right-0 z-50 mx-auto h-16 w-16 rounded-full bg-slate-900/20 p-4 text-slate-200 md:h-20 md:w-20">
		<!--removed animate-bounce during development-->
		<svg
			xmlns="http://www.w3.org/2000/svg"
			viewBox="0 0 24 24"
			fill="none"
			stroke="currentColor"
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
			class="lucide lucide-arrow-down">
			<path d="M12 5v14" />
			<path d="m19 12-7 7-7-7" />
		</svg>
	</div>
</div>

<style lang="postcss">
	.darken-edges {
		background: radial-gradient(
			circle,
			rgba(0, 0, 0, 0) 50%,
			rgba(0, 0, 0, 0.1) 100%
		);
		pointer-events: none;
	}
</style>
