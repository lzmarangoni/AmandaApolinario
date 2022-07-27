<script>
    import DisplayHeader1 from "../atoms/DisplayHeader1.svelte";
    import Paragraph from "../atoms/Paragraph.svelte";

    export let title;
</script>

<DisplayHeader1 withAnimation={false} class="!mt-16 text-dust {$$props.class}">{title}</DisplayHeader1>
<Paragraph class="text-center md:text-left">
   <slot />
</Paragraph>
