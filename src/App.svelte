<script lang="ts">
  import { onMount } from "svelte/internal";
  import Loading from "./lib/Components/Loading.svelte";
  import Header from "./lib/Components/Header.svelte";
  import Content from "./lib/Components/Content.svelte";
  import Contact from "./lib/Components/Contact.svelte";
import Footer from "./lib/Components/Footer.svelte";
  
  let loading: boolean = true;
  onMount(() => {
    setTimeout(() => {
      loading = false
    }, 3000);
  });
</script>

<main>
  {#if loading}
    <Loading />
  {:else}
    <Header />
    <Content />
    <Contact />
    <Footer/>
  {/if}
</main>
