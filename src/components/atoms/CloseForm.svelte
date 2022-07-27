<script>
    import { openModal } from "../../stores/modal";
 </script>
 <a on:click={()=>{$openModal = !$openModal; console.log($openModal) }} class="mx-2 absolute">
     <p class="absolute -top-5 right-2 border-2 w-10 bg-dust rotate-[45deg] rounded-md "></p>
     <p class="absolute -top-5 right-2 border-2 w-10 bg-dust rotate-[135deg] rounded-md"></p>
</a>