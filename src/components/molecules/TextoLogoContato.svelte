<script>
    import AmandaLogo from "../../assets/AmandaLogo.svelte";
</script>

<div class="textoComLogo flex flex-col items-center mr-16">
    <h1 class="font-marisa text-4xl mb-10">AMANDA APOLINÁRIO</h1>
    <div><AmandaLogo class="w-[10em]"/></div>
    <h1 class="font-marisa text-2xl mt-10">ARQUITETURA E INTERIORES</h1>
</div>

<style lang="sass">
@media screen and (max-width: 450px)
    .textoComLogo
        margin-top: 2em
        margin-right: 0

    .textoComLogo h1
        text-align: center
        width: 80vw
        font-size: 1.6em

@media screen and (min-width: 451px) and (max-width: 1200px)
    .textoComLogo h1
        text-align: center
        font-size: 1.6em

    .textoComLogo
        margin-right: 0
</style>
