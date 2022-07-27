
<button class="bg-darkBrown button
    md:my-6 mr-2 px-6 mt-6 text-dust font-marisa
    font-medium rounded py-3 uppercase hover:-translate-y-1  text-[22px] md:text-2xl {$$props.class}">
    <slot />
</button>

<style lang="sass">
    .button
        transition: all .3s ease-in-out
        &:hover
            box-shadow: inset 0 5vw 0 rgba(0,0,0,0.3)

</style>


