<script lang="ts">
	import EditorLine from '$lib/editor-line.svelte';
	import Window from '$lib/window.svelte';

	const skillSets = [
		{
			skillSetHeading: ['Languages'],
			skills: [
				{ name: 'Executive', level: 80 },
				{ name: 'Engineer', level: 85 },
				{ name: 'English', level: 99 }
			]
		},
		{
			skillSetHeading: ['Backend'],
			skills: [
				{ name: 'ASP.NET', level: 95, comment: 'Core, 4x, etc.' },
				{ name: 'Azure Functions', level: 85 },
				{ name: 'Dapr', level: 70 }
			]
		},
		{
			skillSetHeading: ['Data'],
			skills: [
				{ name: 'Cosmos DB', level: 90 },
				{ name: 'Redis', level: 85 },
				{ name: 'SQL Server', level: 75 }
			]
		},
		{
			skillSetHeading: ['Frontend'],
			skills: [
				{ name: 'Svelte/SvelteKit', level: 75 },
				{ name: 'Tailwind', level: 60 },
				{ name: 'React/Next', level: 50 }
			]
		},
		{
			skillSetHeading: ['Cloud'],
			skills: [
				{ name: 'Azure', level: 85 },
				{ name: 'Akamai', level: 40 },
				{ name: 'Cloudflare', level: 35 }
			]
		},
		{
			skillSetHeading: ['CI/CD'],
			skills: [
				{ name: 'Azure DevOps', level: 85 },
				{ name: 'GitHub', level: 40 }
			]
		}
	];
</script>

<div class="bg-slate-200">
	<div class="relative z-40 mx-auto max-w-7xl px-4 pb-6 pt-12">
		<div
			class="absolute top-0 z-0 mx-auto hidden h-full w-full bg-[url('/images/coffee.webp')] bg-right-top bg-no-repeat py-24 bg-blend-normal md:block">
		</div>

		<h2
			class="z-10 font-['Roboto_Mono'] text-xl leading-none tracking-tight text-slate-700 mb-12">
			<span class="mr-1 text-slate-700/50">~/</span>
			I'M GOOD AT...
		</h2>

		<div class="grid gap-12 md:grid-cols-2 lg:grid-cols-3">
			{#each skillSets as o, i}
				<Window>
					{#each o.skillSetHeading as h, j}
						<EditorLine class="text-sky-700"># {h}</EditorLine>
					{/each}
					{#each o.skills as s, j}
						<EditorLine />
						<EditorLine>
							{s.name}
							{#if s.comment}
								<span class="text-slate-400/80"># {s.comment}</span>
							{/if}
						</EditorLine>
						<EditorLine>
							<div class="absolute top-1 w-full pl-10">
								<div class="rounded-full bg-slate-900/75">
									<div
										class="h-1 rounded-full bg-zinc-50 pl-10"
										style="width: {s.level}%">
									</div>
								</div>
							</div>
						</EditorLine>
					{/each}
					{#each Array(11 - (o.skills.length * 3 + o.skillSetHeading.length)) as _, j}
						<EditorLine />
					{/each}
				</Window>
			{/each}
		</div>
	</div>
</div>
