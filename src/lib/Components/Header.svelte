<script lang="ts">
  import gsap, { Power3 } from "gsap";
  import { onMount } from "svelte/internal";
  import Icon from "svelte-icons-pack/Icon.svelte";
  import RiSystemArrowDownSLine from "svelte-icons-pack/ri/RiSystemArrowDownSLine";
  let name_eng;
  let name_thai;
  let btn_click;

  onMount(() => {
    gsap
      .timeline()
      .from(name_eng, {
        opacity: 0,
        y: 40,
        duration: 1,
        ease: Power3.easeInOut,
      })
      .from(name_thai, {
        y: 10,
        duration: 0.7,
        opacity: 0,
        ease: Power3.easeInOut,
      })
      .from(btn_click, { opacity: 0, duration: 0.7, ease: Power3.easeInOut });
  });
</script>

<section class="min-h-screen relative flex-center bg-[#F5F4EF]">
  <div class="text-center p-6">
    <h1 bind:this={name_eng} class="text-xl md:text-2xl text-[#FDA162]">
      Kittipod Lambangchang
    </h1>
    <h1 bind:this={name_thai} class="text-3xl md:text-4xl my-4 ">กิตติพศ หลำบางช้าง</h1>
    <a
      bind:this={btn_click}
      class="text-4xl animate-bounce absolute bottom-[15%] md:bottom-[15%]"
      href="#content"><i class="fa fa-angle-down" /></a
    >
  </div>
</section>
