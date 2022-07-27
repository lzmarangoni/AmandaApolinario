<script>
  import Card from "../atoms/Card.svelte";
</script>

<div class="container flex overflow-auto hover:cursor-pointer">
    <div class="scroll-area self-center">
        <Card fotoURL="./assets/fotos_day_hospital/FOTO-4.webp">Day Hospital</Card>
    </div>
    
      <div class="scroll-area self-center hover:cursor-pointer">
        <Card fotoURL="./assets/fotos_day_hospital/FOTO-8.webp"></Card>
      </div>
    
      <div class="scroll-area self-center hover:cursor-pointer">
        <Card fotoURL="./assets/fotos_day_hospital/FOTO-3.webp"></Card>
      </div>
</div>

<style lang="sass">
.container
  scroll-snap-type: x mandatory

.scroll-area
  scroll-snap-align: start

</style>

