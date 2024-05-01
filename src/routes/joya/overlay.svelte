<script lang="ts">
</script>

<div class="overlay">
    <img src="images/cans-1.webp" alt="First image from artist residency" />
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <img src="images/cans-2.webp" alt="Second image from artist residency" />
    <img src="images/cans-3.webp" alt="Third image from artist residency" />
    <div></div>
    <div></div>
    <div></div>
    <div></div>
    <img src="images/cans-5.webp" alt="Fourth image from artist residency" />
    <img src="images/cans-7.webp" alt="Fifth image from artist residency" />
</div>

<style>
    .overlay {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-template-rows: repeat(5, 1fr);
        max-width: 100dvw;
    }
    img {
        width: 100%;
        border-radius: 0.5rem;
        box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.1);
    }
    

</style>
