<script>
	// @ts-nocheck

	import '../app.css';
	import { darkTheme } from '$lib/store';
	import ThemeSelector from '$lib/Components/ThemeSelector.svelte';
	const themeIcons = ['🌞', '🌙'];
</script>

<main class={`${$darkTheme && 'dark'}`}>
	<div
		class={` min-h-screen font-[Prompt] p-5 text-black flex  bg-white dark:bg-[#001219]  flex-col justify-center items-center overflow-hidden`}
	>
		<ThemeSelector {themeIcons} />
		<div class="max-w-[960px] w-full mx-auto ">
			<slot />
		</div>
	</div>
</main>
