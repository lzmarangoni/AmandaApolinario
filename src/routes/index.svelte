<script lang="ts">
    import IntroPage from "../components/templates/IntroPage.svelte";
    import InitialPage from "../components/templates/InitialPage.svelte";
    import PorqueArquiteturaHospitalar from "../components/templates/PorqueArquiteturaHospitalar.svelte";
    import NossosTrabalhos from "../components/templates/NossosTrabalhos.svelte";
    import Contato from "../components/templates/Contato.svelte";
    import { onMount } from "svelte";
    import {MouseFollower} from "../utils/MouseFollower";
    import Sobre from "../components/templates/Sobre.svelte";
    import Modal from "../components/molecules/Modal.svelte";
    import Formulario from "../components/molecules/Formulario.svelte";

    let follower : HTMLDivElement;
    let smoothScrollingWrapper : HTMLDivElement;
    let largura: any;

    onMount(() => {
        MouseFollower(follower);
        largura = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;
        const body = document.body;
        let height = smoothScrollingWrapper.getBoundingClientRect().height - 1;
        let speed = 0.1;
        let offset = 0;
        body.style.height = Math.floor(height) + "px";
        const smoothScroll = () => {
            offset += (window.pageYOffset - offset) * speed
            let scroll = "translateY(-" + offset + "px) translateZ(0)";
            smoothScrollingWrapper.style.transform = scroll;
            requestAnimationFrame(smoothScroll);
        }
        smoothScroll();
    })

</script>

<Modal><Formulario/></Modal>

<div bind:this={follower} class="border-darkBrown z-10 duration-200 border-2 rounded-full h-6 w-6 fixed top-5 left-5"></div>

<!--<IntroPage />-->

{#if (largura >= 738)}

    <div bind:this={smoothScrollingWrapper}>
        <InitialPage />
        <PorqueArquiteturaHospitalar />
        <NossosTrabalhos />
        <Sobre />
        <Contato />
    </div>
{/if}

{#if (largura < 738)}
    <div>
        <InitialPage />
        <PorqueArquiteturaHospitalar />
        <NossosTrabalhos />
        <Sobre />
        <Contato />
    </div>
{/if}



