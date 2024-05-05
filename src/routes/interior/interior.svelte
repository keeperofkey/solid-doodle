<script lang="ts">
    import { LumaSplatsThree } from "@lumaai/luma-web";
    import * as THREE from "three";
    import { OrbitControls } from "three/addons/controls/OrbitControls";

    let scene = new THREE.Scene();
    let camera = new THREE.PerspectiveCamera(
        75,
        window.innerWidth / window.innerHeight,
        0.1,
        1000,
    );
    camera.position.z = 2;
    let renderer = new THREE.WebGLRenderer();
    let controls = new OrbitControls(camera, renderer.domElement);
    controls.enableDamping = true;
    renderer.domElement.style.position = "absolute";
    renderer.domElement.style.width = "100%";
    renderer.domElement.style.height = "100%";

    document.body.appendChild(renderer.domElement);

    let splats = new LumaSplatsThree({
        source: "https://lumalabs.ai/capture/27130443-941d-430e-b68e-2e09bc0a4998",
        particleRevealEnabled: true,
    });
    scene.add(splats);

    function frameLoop() {
        let canvas = renderer.domElement;
        let width = canvas.clientWidth;
        let height = canvas.clientHeight;

        if (canvas.width !== width || canvas.height !== height) {
            camera.aspect = width / height;
            camera.updateProjectionMatrix();
            renderer.setSize(width, height, false);
        }

        // controls.update();

        renderer.render(scene, camera);
    }

    renderer.setAnimationLoop(frameLoop);
</script>

<style>
</style>
