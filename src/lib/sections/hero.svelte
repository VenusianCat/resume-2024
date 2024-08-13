<script>
	import LinkedIn from '$lib/icons/linked-in.svelte';
</script>

<div
	class="relative flex h-[50vh] w-full flex-col justify-start overflow-hidden bg-cover bg-right bg-no-repeat px-4"
	style="background-image: url('/images/headshot-2.jpg');">
	<ul class="flex items-end justify-between text-slate-700">
		<li
			class="glass mt-4 block p-5 text-sm tracking-tight sm:text-2xl md:text-3xl">
			<!--mock code block-->
			<div
				class="my-2 font-['Roboto_Mono'] font-medium leading-none tracking-tight drop-shadow">
				<p>
					<span class="font-normal text-zinc-100/30">1</span>
					<span class="text-slate-700">&nbsp;&lbrace;</span>
				</p>

				<p>
					<span class="font-normal text-zinc-100/30">2</span>
					&nbsp;&nbsp;
					<span class="text-slate-600">author:</span>
					<span class="text-slate-300">'Richard Tammar'</span><span class="text-slate-600">,</span>
				</p>

				<p>
					<span class="font-normal text-zinc-100/30">3</span>
					&nbsp;&nbsp;
					<span class="text-slate-600">message:</span>
					<span class="text-slate-300">'Hello World!'</span>
				</p>

				<p>
					<span class="font-normal text-zinc-100/30">4</span>
					<span class="text-slate-700">&nbsp;&rbrace;</span>
				</p>
			</div>
			<!-- end mock code block -->
			<!--<p class="font-bold">
				I'm Richard Tammar
			</p>
			<p
				class="mt-0 max-w-[30rem] pt-0 text-sm leading-snug tracking-tight text-slate-700 md:text-base [@media(min-height:600px)]:block">
				Affable, senior technologist with an aptitude for connecting the C-suite
				to the engine room. Curious and analytical, I thrive anywhere I have the opportunity to
			catalyze positive change.
			</p>-->
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

	<!--<div
		class="absolute bottom-12 left-0 right-0 z-50 mx-auto h-16 w-16 rounded-full bg-slate-900/20 p-4 text-slate-200 md:h-20 md:w-20 animate-bounce">
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
	</div>-->
</div>

<style lang="postcss">
	.glass {
		background: rgba(255, 255, 255, 0);
		border-radius: 16px;
		box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
		backdrop-filter: blur(3px);
		-webkit-backdrop-filter: blur(3px);
		border: 1px solid rgba(255, 255, 255, 0.1);
	}
</style>
