<script>

import { onMount } from "svelte";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/dist/ScrollTrigger.js";
import TextoContato from "../atoms/TextoContato.svelte";
import IconsContato from "../molecules/IconsContato.svelte";
import SombraPaginaContato from "../atoms/SombraPaginaContato.svelte";
import AmandaSmallLogo from "../../assets/AmandaSmallLogo.svelte";

onMount(() => {

    gsap.registerPlugin(ScrollTrigger);

    gsap.from(".texto", {
        scrollTrigger: {
            trigger:".contato",
            start: "top center",
            toggleActions: "restart none none reverse",
        },
        x:"100%",
        duration: 3,
        ease:"back(1)",
    })
})
</script>

<section class="flex max-w-screen flex-col bg-dust w-screen overflow-hidden">

        <div class="contato max-w-full relative z-30 items-center py-20 md:p-20 md:overflow-hidden -mb-[22em]">

            <div class="linhaDireita md:w-1.5 h-96 bg-darkBrown absolute md:right-12 invisible md:visible"></div>

            <div class="texto flex justify-between">
                <div class="flex flex-col">
                    <TextoContato />
                    <IconsContato />
                </div>
                <AmandaSmallLogo class="w-64 md:w-80 mx-auto md:mx-0 md:mr-12" />
            </div>
        </div>
    <SombraPaginaContato />
</section>

<style lang="sass">
@media screen and (max-width: 450px)
    .texto
        flex-direction: column

    .linhaDireita
        width: 0
</style>
