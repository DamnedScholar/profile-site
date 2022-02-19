<script>
    // import { readdir } from 'fs/promises'

    import Gallery from 'svelte-image-gallery'

    async function setup() {
        let images = []
        return images
    }
</script>

<Gallery>
    {#await setup}
        Loading
    {:then contents}
        {#each contents as img}
            <img src='{img}' alt='{img}'>
        {/each}
    {/await}
</Gallery>
