<script lang="ts">
  import Icon from "svelte-icons-pack/Icon.svelte";
  import SiSvelte from "svelte-icons-pack/si/SiSvelte";
  import SiReact from "svelte-icons-pack/si/SiReact";
  import SiTailwindcss from "svelte-icons-pack/si/SiTailwindcss";
  import SiSass from "svelte-icons-pack/si/SiSass";
  import SiTypescript from "svelte-icons-pack/si/SiTypescript";
  import SiJavascript from "svelte-icons-pack/si/SiJavascript";
  import SiHtml5 from "svelte-icons-pack/si/SiHtml5";
  import SiCss3 from "svelte-icons-pack/si/SiCss3";
  import SiRedux from "svelte-icons-pack/si/SiRedux";
  import SiGreensock from "svelte-icons-pack/si/SiGreensock";
  import { onMount } from "svelte/internal";
  import gsap, { Power3 } from "gsap";
  import { ScrollTrigger } from "gsap/ScrollTrigger";
  gsap.registerPlugin(ScrollTrigger);
  let title_content;
  let para1;
  let para2;
  let para3;
  let stack;
  //   let content2;

  onMount(() => {
    let timeline = gsap.timeline({
      scrollTrigger: {
        trigger: "#content",
        markers: true,
        start: "top 50%",
        end: 'top 0%',
        // scrub:true
      },
    });
    timeline.from(title_content, {
      delay: 0.1,
      duration: 1,
      opacity: 0,
      y: 30,
      ease: Power3.easeOut,
    }).from(para1,{opacity:0,y:10,duration:0.7,ease:Power3.easeInOut})
    .from(para2,{opacity:0,y:10,duration:0.7,ease:Power3.easeInOut})
    .from(para3,{opacity:0,y:10,duration:0.7,ease:Power3.easeInOut})
    .from(stack,{opacity:0,y:10,duration:0.7,ease:Power3.easeInOut})
  });
</script>

<section id="content" class="text-white flex-center bg-[#FEFEFA] min-h-screen">
  <div class="text-[#091610] max-w-[1440px] w-full">
    <h1 bind:this={title_content} class="text-5xl">ผมเป็นใคร ?</h1>
    <p bind:this={para1} class="text-xl my-6 max-w-[550px]">
      สวัสดี ผมชื่อ <span class="text-[#ef233c]"
        >กิตติพศ หลำบางช้าง (ต้น / กิตต้น)</span
      > อายุ 18 ปี ปัจจุบันเป็นนักศึกษาชั้นปีที่ 1 คณะวิศวกรรมศาสตร์ สาขาวิศวกรรมคอมพิวเตอร์
      สถาบันเทคโนโลยีพระจอมเกล้าเจ้าคุณทหารลาดกระบัง
    </p>
    <p bind:this={para2} class="text-xl max-w-[550px]">
      ผมมีความชื่นชอบในการพัฒนาเว็บไซต์ และมีความสนใจทางด้าน AI และ Data Science
      ซึ่งตอนนี้ผมก็พยายามที่จะเรียนรู้และพัฒนาตัวเองอยู่เสมอ
    </p>
    <div class="mt-6">
      <p bind:this={para3} class="text-xl mb-4">
        และนี่คือ <span class="text-[#ef233c]">Tech Stack</span> ที่ผมใช้
      </p>
      <div bind:this={stack} class="flex">
        <Icon className="mx-2" color="#0a9396" size="32" src={SiSvelte} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiReact} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiTailwindcss} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiSass} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiTypescript} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiJavascript} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiHtml5} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiCss3} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiRedux} />
        <Icon className="mx-2" color="#0a9396" size="32" src={SiGreensock} />
      </div>
    </div>
  </div>
</section>
