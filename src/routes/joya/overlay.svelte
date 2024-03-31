<script lang="ts">
</script>

<div class="overlay">
    <img src="images/cans-1.png" alt="First image from artist residency" />
    <div></div>
    <div></div>
    <img src="images/cans-2.png" alt="Second image from artist residency" />
    <img src="images/cans-3.png" alt="Third image from artist residency" />
    <div></div>
    <div></div>
    <img src="images/cans-5.png" alt="Fourth image from artist residency" />
    <img src="images/cans-7.png" alt="Fifth image from artist residency" />
</div>

<style>
    .overlay {
        /*display items as a checkerd pattern*/
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-template-rows: repeat(2, 1fr);
        max-width: 100dvh;
    }
    img {
        width: 100%;
    }
</style>
