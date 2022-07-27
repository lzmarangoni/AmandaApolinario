<script>
    import Paragraph from "./Paragraph.svelte";
    export let fotoURL = "";
    // export let projetos;
</script>


<div class="card m-auto md:m-6 ml-0 {$$props.class}">
    <img class="max-h-[60vh] shadow-lg w-full rounded" src={fotoURL} alt="">
    <Paragraph class="mt-2 !font-marisa font-bold !text-2xl"><slot/></Paragraph>
</div>

<style lang="sass">
@media screen and (max-width: 415px)
    .card
        width: 80vw
        margin: 1em

@media screen and (min-width: 415px) and (max-width: 738px)
    .card
        width: 40vw
        margin: 1em
</style>