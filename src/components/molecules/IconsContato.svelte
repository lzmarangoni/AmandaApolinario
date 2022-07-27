<script>
    import ButtonPrincipal from "../atoms/ButtonPrincipal.svelte";
    import IconInstagram from "../atoms/IconInstagram.svelte";
    // import IconWhats from "../atoms/IconWhats.svelte";
    import { whats, instagram, email } from "../../utils/Constantes"
import ButtonContato from "../atoms/ButtonContato.svelte";
</script>

<div class="btnContato mx-auto md:mx-0 flex flex-col ">
    <ButtonContato on:click={() => window.open(email)} class="botao">ENTRAR EM CONTATO</ButtonContato>
     <div class="iconsContato mx-auto md:mx-0 my-10 flex">
        <!-- <IconWhats on:click={() => window.open(whats)}/> -->
        <IconInstagram on:click={() => window.open(instagram)} />
     </div>
</div>

<style lang="sass">
    :global.botao
        width: 15em
        font-size: 1.2em

@media screen and (max-width: 450px)
    .btnContato
        align-self: center

</style>
