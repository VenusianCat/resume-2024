<script lang="ts">
	let {
		children,
		icon
	}: {
		children?: any;
		icon?: any;
	} = $props();
</script>

<div class="relative z-50 h-fit rounded-lg py-2 pl-6 pr-8 backdrop-filter backdrop-blur-sm bg-white opacity-60 font-bold text-zinc-700 shadow-lg ">
	<div class="counter-reset-line -ml-2 pt-4 text-sm">
		{@render children()}
	</div>
</div>

<style lang="postcss">
	.counter-reset-line {
		counter-reset: line;
	}
</style>
