<script>
    import ButtonPrincipal from "../atoms/ButtonPrincipal.svelte";
    import DisplayHeader1 from "../atoms/DisplayHeader1.svelte";
    import ButtonSecondary from "../atoms/ButtonSecondary.svelte";
    import {introFinished} from "../../utils/Stores";
    import gsap from "gsap";
    import LogoPattern from "../atoms/LogoPattern.svelte";
    import ButtonContato from "../atoms/ButtonContato.svelte";
   
    export let displayText;
    

    let btns;
   

    $: if ($introFinished) {
        gsap.from(btns, { opacity: 0, y: 200, duration: 3.3, ease: "back(1)"})
    }
</script>

<div class="relative h-full flex flex-col z-10 justify-center items-start mx-10px md:ml-28 md:w-full px-3 md:px-0">
    <DisplayHeader1 withAnimation class="text-darkBrown mx-6">{displayText}</DisplayHeader1>
    <div bind:this={btns} class="flex w-full md:flex-row flex-col md:space-x-5 -mt-32 translate-y-32">
        <ButtonContato class="px-10 text-[22px]">Faça um orçamento</ButtonContato>
        <ButtonSecondary>Saiba Mais</ButtonSecondary>
    </div>
</div>
