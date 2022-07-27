<script>
    import AmandaLogo from "../../assets/AmandaLogo.svelte";
    import ButtonSecondary from "../atoms/ButtonSecondary.svelte";
    import TitleWithText from "../molecules/TitleWithText.svelte";
    import { gsap } from "gsap";
    import { ScrollTrigger } from "gsap/dist/ScrollTrigger.js";
    import { onMount } from "svelte";


    onMount(()=>{
        gsap.registerPlugin(ScrollTrigger);

        gsap.from(".logo",{
            scrollTrigger: {
                trigger:".logo",
                toggleActions: "restart none none reverse",
                start: "top center",
            },
                x:"100%",
                duration: 2,
                ease:"back(1)",
            }
        )

        gsap.from(".texto1",{
                scrollTrigger:{
                    trigger:".titulo",
                    start: "top center",
                    toggleActions: "restart none none reverse",
                },
                x:"100%",
                duration: 2,
                opacity: 0,
                ease:"back(1)",
        })

        gsap.to(".circulo", {
            rotation: 360,
            duration: 3,
            repeat: -1,
            ease: "linear",

        })
    })


</script>

<div class="w-screen min-h-screen relative bg-darkBrown overflow-hidden">
    <div class="w-1 mt-10 md:w-1.5 h-screen bg-dust absolute md:left-8 invisible md:visible"></div>
    <div class="logo relative flex space-x-1 md:space-x-3 mt-16 z-30 ml-16 !opacity-100">
        {#each Array(25).fill(0) as _, index}
            <AmandaLogo class="w-12 text-dust"/>
        {/each}
    </div>

    <div class="-mb-[17em]">

        <div class="texto1 flex h-full mx-auto md:mx-0 px-8 text-center md:px-0 md:ml-28 items-center justify-center">
            <div class="flex-1 mt-5 md:mr-8">
                <TitleWithText class="titulo" title="Por que Arquitetura Hospitalar?">
                    O profissional da Arquitetura Hospitalar tem a capacidade de criar espaços com fluxos bem resolvidos,
                    materiais de acabamento estratégicos e um ambiente acolhedor ao paciente que está em tratamento, seja
                    ele emergencial ou ambulatorial, tudo isso dentro das normas vigentes da vigilância sanitária e normas
                    técnicas construtivas. Para melhores soluções, nossa equipe conta com profissionais multidisciplinares,
                    dentre eles enfermeiras, arquitetos e construtores.
                </TitleWithText>

                <ButtonSecondary class="!text-2xl font-semibold ">
                    Conheça Nosso Trabalho
                </ButtonSecondary>
            </div>

            <div class="flex-1 hidden md:block relative justify-center md:pt-10 py-10 md:pr-20">
            <img class="w-80 h-80 ml-auto bg-dust translate-x-12 relative z-30 rounded-full shadow-lg object-cover" src="./assets/fotos_day_hospital/FOTO-3.webp"  alt="">
            <div class="max-h-[32vw] -mt-36">
                <img class="w-[42vw] shadow-lg h-[42vw] relative mx-auto z-10 bg-dust rounded-full" src="./assets/fotos_day_hospital/FOTO-13.webp" alt="">
            </div>
            <div>
                <p class="p-auto absolute top-[200px] left-[-0.5vw] border-dashed border border-dust h-[44vw] w-[44vw] rounded-full text-white"></p>
            </div>
        </div>
    </div>

        <div class="relative bottom-[20em] w-screen h-96 bg-black opacity-10 -skew-y-6 translate-y-1/3"></div>

    </div>
</div>
