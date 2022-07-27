<script>
    export let label;
    export let placeholder;
    export let name;

</script>

        <div class="pt-4 px-2 relative">
            <textarea rows="10" class=" peer p-2 pl-28 focus:pl-4 my-2 w-full rounded-md focus:bg-dust focus:text-darkBrown font-semibold
             bg-darkBrown text-dust duration-500 {$$props.class} " name={name} label={label} placeholder={placeholder}></textarea>
            <label class="bg-dust text-darkBrown top-[2.1em] px-2 py-1 rounded absolute text-sm left-5 peer-focus:-top-1 peer-focus:bg-darkBrow duration-500" for="nome">{label}</label>
        </div>
