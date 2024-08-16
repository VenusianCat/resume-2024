<script lang="ts">
	import EditorLine from '$lib/editor-line.svelte';
	import Window from '$lib/window.svelte';

	const skillSets = [
		{
			skillSetHeading: ['Bridging Domains'],
			icon: 'fa-magic',
			description: [
				{line:'I '},{line:'the C-suite to the engine'},{line:'room.'}
			]
		},
		{
			skillSetHeading: ['Getting Things Done'],
			icon: 'fa-check-square',
			description: [
				{line:'something goes here'}
			]
		},
		{
			skillSetHeading: ['Encouraging All Voices'],
			icon: 'fa-code-branch',
			description: [
				{line:'/* an aptitude for connecting'},{line:'the C-suite to the engine'},{line:'room. */'}
			]
		},
		{
			skillSetHeading: ['Conveying Ideas'],
			icon: 'fa-lightbulb',
			description: [
				{line:'/* an aptitude for connecting'},{line:'the C-suite to the engine'},{line:'room. */'}
			]
		},
		{
			skillSetHeading: ['Designing Systems'],
			icon: 'fa-cogs',
			description: [
				{line:'/* an aptitude for connecting'},{line:'the C-suite to the engine'},{line:'room. */'}
			]
		},
		{
			skillSetHeading: ['Coding'],
			icon: 'fa-code',
			description: [
				{line:'/* an aptitude for connecting'},{line:'the C-suite to the engine'},{line:'room. */'}
			]
		}
	];

</script>

<div class="bg-gradient-to-tr from-indigo-200 via-red-200 to-yellow-100">
	<div class="relative z-40 mx-auto max-w-7xl px-4 pb-6 pt-12">
		<div
			class="absolute top-0 z-0 mx-auto hidden h-full w-full py-24 bg-blend-normal md:block">
		</div>

		<h2
			class="z-10 mb-12 font-['Roboto_Mono'] text-xl leading-none tracking-tight text-slate-700">
			// Core Skills
		</h2>

		<div class="grid gap-12 md:grid-cols-2 lg:grid-cols-3">
			{#each skillSets as o, i}
				<Window icon={o.icon}>
					{#each o.skillSetHeading as h, j}
						<EditorLine class="text-green-700 font-bold">// {h} 	<!--font awesome test-->

		<span class="fa-stack fa-1x">
			<i class="fas {o.icon} fa-stack-1x fa-inverse text-green-700"></i>
		</span>

	<!--end font awesome test--></EditorLine>
					{/each}
					<EditorLine class="font-normal text-zinc-900">/*</EditorLine>	
					{#each o.description as s, j}
						<EditorLine class="font-normal text-zinc-900">
							{s.line}
						</EditorLine>
					{/each}
					<EditorLine class="font-normal text-zinc-900">*/</EditorLine>
					<EditorLine />
					<!--{#each Array(11 - (o.description.length * 3 + 2)) as _, j}
						<EditorLine />
					{/each}-->
				</Window>
			{/each}
		</div>
	</div>
</div>
