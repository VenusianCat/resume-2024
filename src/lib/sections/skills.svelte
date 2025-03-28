<script lang="ts">
	import EditorLine from '$lib/editor-line.svelte';
	import Window from '$lib/window.svelte';

	const skillSets = [

		{
			skillSetHeading: 'Bridging Domains',
			icon: 'fa-link',
			description:
				'Equally empathetic with executives and engineers, I enjoy the challenge of aligning practice with strategy.'
		},
		{
			skillSetHeading: 'Building Teams',
			icon: 'fa-code-branch',
			description:
				'Warm, approachable and egalitarian, I seek to capitalize on individual talents and foster excellent team dynamics.'
		},
		{
			skillSetHeading: 'Getting Things Done',
			icon: 'fa-check-square',
			description: "I'm deeply pragmatic and have a strong bias for action."
		},
		{
			skillSetHeading: 'Conveying Ideas',
			icon: 'fa-lightbulb',
			description:
				'A trained teacher, my presentations have been described as "Clear, smart, digestible... and highly entertaining."'
		},
		{
			skillSetHeading: 'Designing Systems',
			icon: 'fa-cogs',
			description:
				"Curious and analytical, I like to understand how things work and then improve upon them."
		},
		{
			skillSetHeading: 'Coding',
			icon: 'fa-code',
			description:
				'Full-stack development, from SQL to Svelte, since childhood.'
		}
	];

	function splitStringWithoutBreakingWords(str: string, l: number) {
		var strs = [];
		while (str.length > l) {
			var pos = str.substring(0, l).lastIndexOf(' ');
			pos = pos <= 0 ? l : pos;
			strs.push(str.substring(0, pos));
			var i = str.indexOf(' ', pos) + 1;
			if (i < pos || i > pos + l) i = pos;
			str = str.substring(i);
		}
		strs.push(str);
		return strs;
	}
	let x;
</script>

<div class="bg-sky-100 py-4">
	<div class="relative z-40 mx-auto max-w-7xl px-4 pb-6 pt-6">
		<h2
			class="relative z-10 mx-auto mb-6 font-['Roboto_Mono'] text-xl leading-none tracking-wide text-slate-900 sm:mb-10">
			// SUPERPOWERS
		</h2>

		<div class="grid gap-4 sm:gap-8 md:grid-cols-2 lg:grid-cols-3">
			{#each skillSets as o, i}
				<Window icon={o.icon}>
					<EditorLine class="text-white sm:text-base text-sm">
						{o.skillSetHeading}&nbsp;<!--font awesome icon-->
						<i class="fas {o.icon} white"></i>
						&nbsp;
						<!--end font awesome icon-->
					</EditorLine>


					{#each splitStringWithoutBreakingWords(o.description, 40) as s, j}
						<EditorLine class="text-slate-300 tracking-tighter sm:text-sm text-xs">
							{s}
						</EditorLine>
					{/each}

				</Window>
			{/each}
		</div>
	</div>
</div>

<style lang="postcss">
	i {
		position: relative;
		top: 0px;
	}
</style>
