<script lang="ts">
    import AmandaLogo from "../../assets/AmandaLogo.svelte";
    import gsap from "gsap";
    import {createEventDispatcher, onMount} from "svelte";

    let dispatch = createEventDispatcher<{complete: {}}>();

    onMount(() => {
        let config = {
            opacity: 0,
            scale: 0.95,
            translateY: 5,
            stagger: {each: 0.1, from: "start", grid: "auto",},
            duration: 0.5,
        }
        let timeline = gsap.timeline();
        timeline.from(".logo", config);
        timeline.to(".logo", {
            opacity: 0, duration: 0.5, stagger: {each: 0.1, grid: "auto"},
            onComplete: () => { dispatch("complete", {}) }
        }, "-=40%");

    })
</script>

<div class="flex-col max-w-[100vw] items-center justify-center max-h-[100vh] overflow-hidden">
    {#each Array(13).fill(0) as _, index}
        <div class="flex w-[200vw] {(index % 2 === 0) && '-translate-x-12'} md:space-x-4 space-x-0.5"> <!-- Line -->
            {#each Array(20).fill(0) as _}
                <AmandaLogo
                        class="logo relative opacity-100 text-dust md:min-h-24 min-w-24 w-24 md:h-24 my-3 md:my-5 "/>
            {/each}
        </div>
    {/each}
</div>
