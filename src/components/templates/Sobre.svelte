<script>
    import TextoSobre from "../atoms/TextoSobre.svelte";
    import ImagensLaterais from "../molecules/ImgLateralSobre.svelte";
</script>

<section class="sobre flex flex-col w-screen md:flex-row justify-between bg-[#484544] pt-[5em]">
    <div class="w-1 mt-28 md:w-1.5 h-screen bg-dust absolute md:right-12 invisible md:visible"></div>
    <ImagensLaterais />
    <TextoSobre />
</section>


<style lang="sass">
@media screen and (max-width: 1024px)
    .sobre
        flex-direction: column
        padding-top: 12em
</style>