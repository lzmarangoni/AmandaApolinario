<script>
import TitleWithText from "../molecules/TitleWithText.svelte";
import { onMount } from "svelte";
import FotosNossosTrabalhosTelaMaior738px from "../molecules/FotosNossosTrabalhosTelaMaior738px.svelte";
import FotosNossosTrabalhosTelaMenor738px from "../molecules/FotosNossosTrabalhosTelaMenor738px.svelte";
import FiltrosNossosTrabalhos from "../molecules/FiltrosNossosTrabalhos.svelte";
import { gsap }  from "gsap";
import { ScrollTrigger } from "gsap/dist/ScrollTrigger"
let largura = 1300;

onMount(() => {

    largura = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;

    setTimeout(() => {
        gsap.registerPlugin(ScrollTrigger);
        gsap.from(".card", {
            scrollTrigger: {
                trigger: ".nossosTrabalhos",
                toggleActions: "restart none none reverse",
                start: "top 20%",
            },
            y:"100%",
            duration: 1,
            ease:"back(1)",
            opacity: 0,
            stagger: 0.1,
        })

    }, 150);
});
</script>

<div class="w-1 justify-center md:w-1.5 h-screen bg-dust absolute md:left-8 z-30 invisible md:visible"></div>

<div class="w-screen h-screen bg-[#484544] nossosTrabalhos">
    <div class="md:pt-10 md:pl-28 py-10 px-6 flex flex-col">
        <TitleWithText class="!mt-0" title="Nossos trabalhos">
<!--        Clique para ver mais detalhes.-->
        </TitleWithText>
        {#if (largura > 738)}
            <div class="flex flex-col mx-auto md:flex-row">
                <FotosNossosTrabalhosTelaMaior738px />
            </div>
        {:else}
            <FotosNossosTrabalhosTelaMenor738px />
        {/if}

             <FiltrosNossosTrabalhos />

    </div>
</div>
