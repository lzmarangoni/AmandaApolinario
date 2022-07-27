<script>
import Whatsapp from "../../assets/Whatsapp.svelte";

</script>

<div class="whats bg-darkBrown m-2 w-16 h-16
rounded-full p-4 hover:cursor-pointer hover:-translate-y-1 text-dust {$$props.class} ">
<Whatsapp on:click />
</div>


<style lang=sass>
:global(.whats)
    transition: all .3s ease-in-out
    &:hover
        box-shadow: inset 0 5vw 0 rgba(0,0,0,0.3)
</style>
