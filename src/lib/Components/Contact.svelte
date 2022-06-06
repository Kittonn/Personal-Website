<script lang="ts">
    import Icon from 'svelte-icons-pack/Icon.svelte';
    import AiFillGithub from "svelte-icons-pack/ai/AiFillGithub";
    import AiOutlineInstagram from "svelte-icons-pack/ai/AiOutlineInstagram";
    import AiFillFacebook from "svelte-icons-pack/ai/AiFillFacebook";
</script>

<section class="min-h-screen text-center flex-center bg-[#F5F4EF]">
    <div>
        <h1 class="text-4xl ">ต้องการติดต่อกับผมหรอ ?</h1>
        <p class="text-xl mt-4 mb-10">ถ้าอยากคุยกับผม หรือมีเรื่องอะไรที่ต้องการปรึกษา สามารถทักผมมาได้ตลอดเวลาเลย</p>
        <div class="flex justify-center items-center">
            <Icon className="mx-2" color="#0a9396" size="40" src={AiFillGithub}/>
            <Icon className="mx-2" color="#0a9396" size="40" src={AiOutlineInstagram}/>
            <Icon className="mx-2" color="#0a9396" size="40" src={AiFillFacebook}/>
        </div>
    </div>
</section>