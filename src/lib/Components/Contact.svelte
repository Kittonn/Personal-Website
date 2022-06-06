<script lang="ts">
  import Icon from "svelte-icons-pack/Icon.svelte";
  import AiFillGithub from "svelte-icons-pack/ai/AiFillGithub";
  import AiOutlineInstagram from "svelte-icons-pack/ai/AiOutlineInstagram";
  import AiFillFacebook from "svelte-icons-pack/ai/AiFillFacebook";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  import gsap, { Power3 } from "gsap";
  import { onMount } from "svelte/internal";
  gsap.registerPlugin(ScrollTrigger);

  let icon;
  let text_head;
  let text_para;

  onMount(() => {
    let timeline = gsap.timeline({
      scrollTrigger: {
        // markers: true,
        trigger: "#contact",
        start: "top 50%",
        end: "top 0%",
        scrub: true,
      },
    });
    timeline
      .from(text_head, {
        duration: 0.7,
        opacity: 0,
        y: 30,
        ease: Power3.easeInOut,
      })
      .from(text_para, {
        duration: 0.7,
        opacity: 0,
        y: 30,
        ease: Power3.easeInOut,
      })
      .from(icon, { duration: 0.7, opacity: 0, y: 30, ease: Power3.easeInOut });
  });
</script>

<section id="contact" class="min-h-screen text-center flex-center bg-[#F5F4EF]">
  <div class="p-6">
    <h1 bind:this={text_head} class="text-2xl md:text-4xl ">ต้องการติดต่อกับผมหรอ ?</h1>
    <p bind:this={text_para} class="text-md md:text-xl mt-4 mb-10">
      ถ้าอยากคุยกับผม หรือมีเรื่องอะไรที่ต้องการปรึกษา
      สามารถทักผมมาได้ตลอดเวลาเลย
    </p>
    <div bind:this={icon} class="flex justify-center items-center">
      <a href="https://github.com/kittonn" target="_blank"><Icon className="mx-2" color="#0a9396" size="40" src={AiFillGithub} /></a>
      <a href="https://instagram.com/kitton._" target="_blank"><Icon
        className="mx-2"
        color="#0a9396"
        size="40"
        src={AiOutlineInstagram}
      /></a>
      <a href="https://facebook.com/thunder2004" target="_blank"><Icon className="mx-2" color="#0a9396" size="40" src={AiFillFacebook} /></a>
    </div>
  </div>
</section>
