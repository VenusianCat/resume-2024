<script>
	import LinkedIn from '$lib/icons/linked-in.svelte';
</script>

<div
	class="w-full flex-col justify-start overflow-hidden md:bg-cover md:bg-right md:bg-no-repeat md:bg-[url('/images/headshot-2.jpg')]">

		
		<div class="tracking-tight md:text-3xl px-4 hidden sm:block">
			
			<!--author block, code block style-->
			<div
				class="glass my-3 font-['Roboto_Mono'] font-medium leading-none tracking-tight drop-shadow hidden sm:inline-block">
				<p>
					<span class="font-normal text-zinc-100/30 border-r-2 pr-2 border-zinc-100/10 inline-block">1</span>
					<span class="text-slate-700 inline-block">&lbrace;</span>
				</p>

				<p>
					<span class="font-normal text-zinc-100/30 border-r-2 pr-2 border-zinc-100/10 inline-block">2</span>
					&nbsp;
					<span class="text-slate-600 inline-block">author:&nbsp;'</span><span class="text-slate-300 inline-block">Richard Tammar</span><span class="text-slate-600">'&nbsp;</span>
				</p>

				<p>
					<span class="font-normal text-zinc-100/30 border-r-2 pr-2 border-zinc-100/10 inline-block">3</span>
					<span class="text-slate-700 inline-block">&rbrace;</span>
				</p>
			</div>
		</div>
		<!-- end code block style -->
		<!--author block, mobile-->
		<h1 class="font-['Roboto_Mono'] sm:hidden text-3xl font-medium tracking-tight pt-2 bg-sky-100 text-slate-700 px-4">Richard Tammar</h1>

		<div class="bg-slate-500 sm:hidden"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1000 100" fill="#e0f2fe"><path d="M0 0v90.2C49.7 99.9 105 82 160 65c75.5-23.3 145.5-22.4 222-3 63 16 119 14 173-8 79.5-32.4 156.2-27.6 240-10 82.6 17.4 143-1 205-31.7V0H0Z"></path></svg></div>
		
		<p class="sm:max-w-[40rem] pt-6 pb-8 sm:text-lg text-slate-100/90 leading-6 pl-4 pr-3 bg-slate-500 sm:bg-transparent"><img src="/images/headshot-square.jpg" alt="headshot of Richard Tammar" class="size-24 rounded-full visible sm:hidden float-right" />
			Veteran technologist with a knack for connecting the C-suite to the
			engine room. Empathetic, curious and analytical, I work to catalyze positive
			change.
		</p>
			<!--mock code block-->

	<!-- end mock code block -->

		
		<div class="absolute top-1 right-1 text-slate-700">
			<a
				href="https://www.linkedin.com/in/richard-tammar/"
				class="-mr-1 block h-12 w-12 p-1">
				<LinkedIn />
			</a>
		</div>

</div>

<style lang="postcss">
	.glass {}
	@media screen and (min-width: 480px) {
		.glass {
			background: rgba(255, 255, 255, 0);
			border-radius: 16px;
			box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
			backdrop-filter: blur(3px);
			-webkit-backdrop-filter: blur(3px);
			border: 1px solid rgba(255, 255, 255, 0.1);
			padding: 1.25rem;
		}
	}
</style>
