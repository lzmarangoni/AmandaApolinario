<script>
    import LottieAnimation from "../atoms/LottieAnimation.svelte";
    import LogoPattern from "../atoms/LogoPattern.svelte";
    import {introFinished} from "../../utils/Stores.ts";
    let finishedFirst = false;
    let allFinished = false;
</script>

<div class="h-screen fixed top-0 left-0 z-50 flex w-full {allFinished && 'invisible opacity-0'} opacity-1 duration-500 items-center flex-wrap justify-center bg-darkBrown">
    { #if !allFinished}
        {#if !finishedFirst}
            <LottieAnimation
                    class="relative -translate-x-1/2 ml-[50%]"
                    on:complete={() => {
                        finishedFirst = true;
                 }} pathAnimation="https://assets10.lottiefiles.com/private_files/lf30_xciqpjma.json"/>
        {:else}
            <LogoPattern on:complete={() => { allFinished = true; $introFinished = true; }}/>
        {/if}
    {/if}
</div>
