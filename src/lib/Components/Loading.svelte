<script lang="ts">
  import { onMount } from "svelte";
  import gsap, { Power3 } from "gsap";
  let text;

  onMount(() => {
    gsap.from(text, { opacity: 0, duration: 2, ease: Power3.easeIn });
    // return () => gsap.killTweensOf(text);
  });
</script>

<section
  class="flex-center text-[#edf2f4] min-h-screen bg-[#2b2d42] text-2xl md:text-6xl"
>
  <h1 bind:this={text} class="text-center">กิตติพศ หลำบางช้าง</h1>
</section>
