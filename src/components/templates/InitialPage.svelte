<script lang="ts">
    import Apresentation from "../molecules/Apresentation.svelte";
    import LottieAnimation from "../atoms/LottieAnimation.svelte";
    import SmallText from "../atoms/SmallText.svelte";
    import LogoSided from "../../assets/LogoSided.svelte";
</script>

<div class="bg-dust h-screen w-screen overflow-x-hidden relative">
    <LogoSided class=" absolute z-50 lg:left-28 ml-[8%] lg:left-0 w-5/6 lg:w-1/3 top-10 text-darkBrown" />
    <div class="w-1 md:w-1.5 h-screen bg-darkBrown absolute md:right-12 invisible md:visible"></div>
    <div class="flex items-center h-full w-full ml-5 mr-10 md:ml-0 md:mr-0  ">
     <Apresentation  displayText={"Projetar Estabelecimentos Assistenciais de Saúde é um trabalho " +
     "que exige conhecimento, dedicação e humanização"}  />
    <div class="top-0 z-30 relative -translate-x-[-20vw] w-3/4 md:-ml-80  translate-x-full h-screen bg-darkBrown -z-10 opacity-20 -skew-x-12"></div>
    </div>
    <div class="absolute hidden md:flex top-[85vh] h-24 left-10 md:left-20 items-center">
        <LottieAnimation class="w-20" loop={true}  pathAnimation="https://assets6.lottiefiles.com/private_files/lf30_n1s3weq5.json"/>
        <SmallText class="text-darkBrown translate-y-3">Arraste para <br />baixo</SmallText>
    </div>
    <div class="absolute w-[700px] overflow-hidden h-screen bg-darkBrown opacity-60 -skew-x-12 top-0 -right-20  z-2">
        <img class="skew-x-12 scale-150 saturate-[1.2]  opacity-30 md:opacity-40 translate-y-32" src="./assets/amanda.webp" />
    </div>
</div>
