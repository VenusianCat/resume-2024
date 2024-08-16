<script lang="ts">
	let {
		children,
		icon
	}: {
		children?: any;
		icon?: any;
	} = $props();
</script>

<div class="relative z-50 h-fit rounded-lg py-2 pl-6 pr-8 backdrop-filter backdrop-blur-sm bg-white opacity-60 font-bold text-zinc-700 shadow-lg">
	<!--font awesome test-->
	<!--
	<div class="-top--1 absolute -right-1">
		<span class="fa-stack fa-1x">
			<i class="fas fa-circle fa-stack-2x text-slate-600/5"></i>
			<i class="fas {icon} fa-stack-1x fa-inverse text-sky-700"></i>
		</span>
	</div>-->
	<!--end font awesome test-->

	<div class="counter-reset-line -ml-2 pt-4 text-sm">
		{@render children()}
	</div>
</div>

<style lang="postcss">
	.counter-reset-line {
		counter-reset: line;
	}
</style>
