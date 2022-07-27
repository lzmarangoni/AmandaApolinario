<script>
    import { openModal } from "../../stores/modal";  
</script>
<div class="{$openModal ? 'right-0' : '-right-[105vw]' }  bg-black backdrop-blur-sm bg-opacity-70 fixed top-0 h-full w-full duration-500 z-[500]">
    <slot/>
</div>

