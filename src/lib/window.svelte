<script lang="ts">
	let {
		children
	}: {
		children?: any;
	} = $props();
</script>

<div class="relative z-50 h-fit rounded-lg py-4 pl-6 pr-8 dark blurred h-full">

	<div class="counter-reset-line -ml-2 pt-4 text-sm">
		{@render children()}
	</div>
</div>

<style lang="postcss">
	.counter-reset-line {
		counter-reset: line;
	}

	.dark.blurred {
		@apply bg-gradient-to-br from-slate-300/70 to-slate-200/70 text-zinc-700 font-bold shadow-lg;
		backdrop-filter: blur(5px);
	}
</style>
