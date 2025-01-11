<script>
</script>

<code
	class={$$restProps.class +
		" relative block overflow-hidden text-ellipsis whitespace-nowrap break-words font-['Roboto_Mono'] before:mr-3 before:inline-block before:w-5 before:border-r-2 before:border-r-gray-300/10 before:pr-1 before:text-right before:text-sm before:text-gray-300/50"}>
	<slot />
</code>

<style lang="postcss">
	code {
		counter-increment: lineNumber;
	}

	code::before {
		content: counter(lineNumber);
		user-select: none;
		-webkit-user-select: none;
	}
</style>
