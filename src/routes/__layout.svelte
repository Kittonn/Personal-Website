<script>
	import '../app.css';
</script>

<header class="absolute top-0 right-0">
	<p class="cursor-pointer">change</p>
</header>
<main
	class="min-h-screen font-[Prompt] p-5 text-black dark:text-[#e0fbfc] flex bg-white dark:bg-[#001219] flex-col justify-center items-center overflow-hidden"
>
	<div class="max-w-[960px] w-full mx-auto ">
		<slot />
	</div>
</main>
