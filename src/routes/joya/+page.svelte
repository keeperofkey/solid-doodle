<script lang="ts">
    import Joya from "./joya.svelte";
    import Overlay from "./overlay.svelte";
</script>

<body>
    <div class="container">
        <Joya />
    </div>
    <Overlay />
</body>

<style>
    .container {
        height: 800dvh;
    }
</style>
