<script lang="ts">
</script>

<code
	class={$$restProps.class +
		" relative block overflow-hidden text-ellipsis whitespace-nowrap break-words font-['Inter'] before:mr-4 before:inline-block before:w-5 before:border-r-2 before:border-r-zinc-200 before:pr-2 before:text-right before:font-['Roboto_Mono'] before:text-sm before:text-zinc-300"}>
	<slot />
</code>

<style lang="postcss">
	code {
		counter-increment: line;
	}

	code::before {
		content: counter(line);
		user-select: none;
		-webkit-user-select: none;
	}
</style>
