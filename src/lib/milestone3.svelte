<script lang="ts">
	export let heading = '';
	export let subheading = '';
	export let body = '';
	export let keywords: string[] = [];
	export let from = '';
	export let to = '';
	export let logo = '';
	export let honors = '';
	export let active = false;
	import { base } from '$app/paths';
</script>

<div
	class="milestone relative mx-auto flex max-w-3xl items-start justify-center sm:pl-8 sm:before:absolute sm:before:inset-0 sm:before:-left-72 sm:before:h-[1px] sm:before:w-1/2 sm:before:bg-gradient-to-r sm:before:from-white/25 sm:before:to-transparent"
	class:active>
	<!-- Date -->
	<time
		class="glass text-normal hidden h-20 w-48 shrink-0 items-center justify-center rounded-bl border border-b-black/10 border-l-white/10 border-r-black/10 border-t-white/10 bg-white/20 p-2 font-['Roboto_Mono'] text-slate-300 shadow sm:flex">
		{#if from !== to}
			{from} - {to}
		{:else}
			{from}
		{/if}
	</time>
	<!-- Card -->
	<div
		class="glass w-full rounded-lg rounded-b-lg rounded-r-lg border border-b-black/10 border-l-white/10 border-r-black/10 border-t-white/10 bg-white/10 p-4 shadow sm:rounded-tl-none sm:p-6">
		<div>
			{#if logo}
				<div class="flex justify-between gap-4">
					<div>
						<h2 class="mb-2 text-lg font-bold text-slate-200 sm:text-xl">
							{@html heading}
						</h2>
						<h3 class="font-bold text-pink-400 drop-shadow lg:text-base">
							{subheading}
							<span class="visible sm:invisible">({to})</span>
						</h3>
					</div>
					<img src="{base}{logo}" alt={subheading} class="size-16 rounded-lg" />
				</div>
			{:else}
				<h2 class="mb-2 text-lg font-bold text-slate-200 sm:text-xl">
					{@html heading}
				</h2>
				<h3 class="font-bold text-pink-400 drop-shadow lg:text-base">
					{subheading}
					<span class="visible sm:invisible">({to})</span>
				</h3>
			{/if}
			{#if honors}<h3 class="mt-2 text-sm text-slate-100">
					honors: <span class="italic">{honors}</span>
				</h3>{/if}
		</div>
		<div
			class="col-span-2 mt-2 flex flex-col gap-4 text-pretty text-xs text-slate-200 sm:text-sm">
			{#if body}
				<p class="leading-normal tracking-normal">{@html body}</p>
			{/if}
			<div class="my-4">
				<ul
					class="flex flex-wrap gap-1 font-['Roboto_Mono'] text-[0.7rem] leading-snug tracking-wide text-white/75">
					{#each keywords as keyword}
						<li class="rounded-full bg-black/20 px-2 py-0.5">{keyword}</li>
					{/each}
				</ul>
			</div>
		</div>
	</div>
</div>
