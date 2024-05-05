<script lang="ts">
    import { LumaSplatsSemantics, LumaSplatsThree } from "@lumaai/luma-web";
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
    const color = new THREE.Color(0xff0000);
    let renderer = new THREE.WebGLRenderer();
    let controls = new OrbitControls(camera, renderer.domElement);
    controls.enableDamping = true;
    renderer.domElement.style.position = "fixed";
    renderer.domElement.style.zIndex = "-1";
    renderer.domElement.style.width = "100%";
    renderer.domElement.style.height = "100%";

    document.body.appendChild(renderer.domElement);
    // document.body.append(renderer.domElement);
    const boxmin = new THREE.Vector3(-1, -1, -1);
    const boxmax = new THREE.Vector3(1, 1, 1);

    let splats = new LumaSplatsThree({
        source: "https://lumalabs.ai/capture/27130443-941d-430e-b68e-2e09bc0a4998",
        particleRevealEnabled: false,
    });
    // splats.onLoad = () => {
    //     splats.captureCubemap(renderer).then((capturedTexture) => {
    //         scene.environment = capturedTexture;
    //         scene.background = color;
    //         scene.backgroundBlurriness = 5;
    //     });
    // };
    scene.add(splats);
    splats.semanticsMask = LumaSplatsSemantics.ALL;
    splats.boundingBox.set(boxmin, boxmax);
    splats.boundingBox.max = boxmax;
    splats.boundingBox.min = boxmin;
    console.log(splats);

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
