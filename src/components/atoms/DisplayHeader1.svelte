<script>
    import {SplitText} from "../../utils/SplitText.ts";
    import gsap from "gsap";
    import {introFinished} from "../../utils/Stores.ts";
    import {onMount} from "svelte";

    let text;
    export let withAnimation;

    $: if ($introFinished) {
        if (withAnimation) {
            let words = SplitText(text, "1").words;
            gsap.from(words, {
                y: 200,
                rotate: 5,
                opacity: 0,
                duration: 0.6,
                stagger: 0.3,
            })
        }
    }
</script>

<h1 bind:this={text} class="md:text-5xl overflow-y-hidden text-3xl text-center md:-mt-3
        md:text-left font-marisa font-bold uppercase {$$props.class}">
    <slot />
</h1>
