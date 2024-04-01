<script lang="ts">
</script>

<div class="overlay">
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img src="images/cans-1.png" alt="First image from artist residency" />
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img src="images/cans-2.png" alt="Second image from artist residency" />
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
    <!-- svelte-ignore a11y-img-redundant-alt -->

    <img src="images/cans-3.png" alt="Third image from artist residency" />
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
    <!-- svelte-ignore a11y-img-redundant-alt -->

    <img src="images/cans-5.png" alt="Fourth image from artist residency" />
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
    <!-- svelte-ignore a11y-img-redundant-alt -->

    <img src="images/cans-7.png" alt="Fifth image from artist residency" />
</div>

<style>
    .overlay {
        /*display items as a checkerd pattern*/
        display: grid;
        grid-template-columns: repeat(auto-fit, 1fr);
        grid-template-rows: repeat(auto-fit, 1fr);
        grid-row-gap: 1rem;
        max-width: 100dvw;
    }
    img {
        width: 100%;
        border-radius: 0.5rem;
        box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.1);
    }
</style>
