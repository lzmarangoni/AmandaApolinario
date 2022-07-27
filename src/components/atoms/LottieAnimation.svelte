<script lang="ts">
    import {createEventDispatcher, onMount} from "svelte";
    import Lottie from "lottie-web";

    let component;
    export let pathAnimation;
    export let loop = false;

    const dispatch = createEventDispatcher<{complete: {}}>();

    onMount(() => {
            let animation = Lottie.loadAnimation({
                path: pathAnimation,
                container: component,
                renderer: "svg",
                loop: loop,
            })
            animation.addEventListener("complete", () => {
                dispatch("complete", {});
            })
    })
</script>

<div class="{$$props.class}" bind:this={component}></div>
