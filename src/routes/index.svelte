<script lang="ts">
	import { onMount } from 'svelte';
	import { fade, fly } from 'svelte/transition';
	import { cubicInOut } from 'svelte/easing';
	import LogoGithub from 'carbon-icons-svelte/lib/LogoGithub.svelte';
	import LogoInstagram from 'carbon-icons-svelte/lib/LogoInstagram.svelte';
	import LogoFacebook from 'carbon-icons-svelte/lib/LogoFacebook.svelte';
	import LogoTwitter from 'carbon-icons-svelte/lib/LogoTwitter.svelte';

	let ready = false;

	onMount(() => {
		ready = true;
	});
</script>

{#if ready}
	<div transition:fade={{ duration: 1000, easing: cubicInOut }}>
		<div in:fly={{ y: 200, duration: 1000 }}>
			<img
				class="w-[200px] h-[200px] md:w-[250px] md:h-[250px] mx-auto rounded-full"
				src="picture.png"
				alt=""
			/>
			<div class="text-center">
				<h1 class="text-xl md:text-3xl mt-3 text-white">Kittipod Lambangchang</h1>
				<p class="text-[15px]  md:text-xl mt-2  italic">
					A passionate computer engineering student.
				</p>
			</div>
			<div class="w-full my-4 h-[4px]">
				<div class="bg-[#005f73] w-[25%] h-full float-left" />
				<div class="bg-[#e9d8a6] w-[25%] h-full float-left" />
				<div class="bg-[#ca6702] w-[25%] h-full float-left" />
				<div class="bg-[#ae2012] w-[25%] h-full float-left" />
			</div>
			<div class="flex flex-row justify-around max-w-[700px] w-full mx-auto flex-wrap items-center">
				<a
					target="_blank"
					href="https://www.github.com/Kittonn"
					class="flex  my-2 w-[150px] justify-center border-2 py-1 px-3  border-[#e0fbfc] rounded-lg items-center"
				>
					<LogoGithub size={32} />
					<p class="ml-2 md:text-lg">Github</p>
				</a>
				<a
					target="_blank"
					href="https://www.instagram.com/kitton._"
					class="flex  my-2 w-[150px]  justify-center border-2 py-1 px-3 border-[#e0fbfc] rounded-lg items-center"
				>
					<LogoInstagram size={32} />
					<p class="ml-2 md:text-lg">Instagram</p>
				</a>
				<a
					target="_blank"
					href="https://web.facebook.com/Thunder2004/"
					class="flex my-2 w-[150px] justify-center border-2 py-1 px-3 border-[#e0fbfc] rounded-lg items-center"
				>
					<LogoFacebook size={32} />
					<p class="ml-2 md:text-lg">Facebook</p>
				</a>
				<a
					target="_blank"
					href="https://twitter.com/kittonofficial"
					class="flex my-2 w-[150px] justify-center border-2 py-1 px-3 border-[#e0fbfc] rounded-lg items-center"
				>
					<LogoTwitter size={32} />
					<p class="ml-2 md:text-lg">Twitter</p>
				</a>
			</div>
		</div>
	</div>
{/if}
