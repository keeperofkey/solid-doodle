<script lang="ts">
    import Joya from "./joya.svelte";
    import Overlay from "./overlay.svelte";
    import Splat from "./splat.svelte";
</script>

<body>
    <div class="container">
        <Joya />
    </div>
    <Overlay />
    <!-- <div class="frame"> -->
    <!--     <Splat /> -->
    <!-- </div> -->
</body>

<style>
    .container {
        height: 800dvh;
    }
    .frame {
        padding-top: 1rem;
    }
</style>
