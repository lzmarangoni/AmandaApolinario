<script>
    export let label;
    export let placeholder;
    export let type;
    export let name;


</script>

        <div class="pt-4 px-2 relative w-full {$$props.class}">
            <input class="peer p-2 pl-24 focus:pl-4 my-2 w-full rounded-md focus:bg-dust focus:text-darkBrown font-semibold
             bg-darkBrown text-dust duration-500 " type={type} name={name} id={label} placeholder={placeholder} required>
            <label class="bg-dust text-darkBrown px-2 py-1 rounded absolute top-[2.1em] left-5 peer-focus:top-1 text-sm peer-focus:bg-darkBrow duration-500" for="nome">{label}</label>
        </div>

