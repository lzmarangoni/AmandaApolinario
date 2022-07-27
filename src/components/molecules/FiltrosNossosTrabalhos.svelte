<script>
    import ButtonPrincipal from "../atoms/ButtonPrincipal.svelte";
</script>

<div class="btnFiltros flex">
    <ButtonPrincipal>Filtro 1</ButtonPrincipal>
    <ButtonPrincipal>Filtro 2</ButtonPrincipal>
    <ButtonPrincipal>Filtro 3</ButtonPrincipal>
</div>

<style lang="sass">
@media screen and (max-width: 415px)
    .btnFiltros
        display: flex
        flex-direction: column
        margin-bottom: 0em
</style>