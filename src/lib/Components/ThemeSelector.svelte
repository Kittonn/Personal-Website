<script lang="ts">
	import { darkTheme } from '$lib/store';
	export let themeIcons: string[];
</script>

<div class="text-xs sm:text-base fixed top-0 right-0 p-2 z-10 text-white dark:text-black">
	<p
		on:click={() => ($darkTheme = !$darkTheme)}
		class="cursor-pointer select-none text-center text-lg rounded"
	>
		{$darkTheme ? themeIcons[0] : themeIcons[1]}
	</p>
</div>
