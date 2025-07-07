<script setup>
import { onMounted } from "vue";
import lottie from "lottie-web";

// Import animasi (bisa diganti ke file animasi yang berbeda)
import mainAnimation from "../assets/front.json";
import anim1 from "../assets/html.json";
import anim2 from "../assets/js.json";
import anim3 from "../assets/python.json";

onMounted(() => {
    // Animasi utama di atas
    lottie.loadAnimation({
        container: document.getElementById("main-lottie"),
        renderer: "svg",
        loop: true,
        autoplay: true,
        animationData: mainAnimation,
    });

    // Animasi untuk masing-masing card
    const animations = [
        { id: "card-lottie1", data: anim1 },
        { id: "card-lottie2", data: anim2 },
        { id: "card-lottie3", data: anim3 },
    ];

    animations.forEach((item) => {
        lottie.loadAnimation({
            container: document.getElementById(item.id),
            renderer: "svg",
            loop: true,
            autoplay: true,
            animationData: item.data,
        });
    });
});
</script>

<template>
    <div class="skil">
        <div class="container text-start py-3">
            <h1 class="text-white fw-bold">Skills</h1>

            <div class="my-4" style="max-width: 500px; margin: auto">
                <div
                    id="main-lottie"
                    style="height: 300px"
                    data-aos="zoom-in"
                ></div>
            </div>

            <div class="row justify-content-center g-4">
                <h4><strong>Apa yang Saya Bisa?</strong></h4>
                <h6 class="ha1">
                    
                    Dunia teknologi selalu berkembang, dan saya senang menjadi
                    bagian dari perjalanan itu. Mulai dari mendesain antarmuka
                    menarik hingga membangun website dinamis, berikut adalah
                    beberapa skill yang saya kuasai dan gunakan untuk mewujudkan
                    ide-ide menjadi nyata.
                </h6>
                <div class="col-md-4">
                    <div class="card p-3 text-center shadow">
                        <div id="card-lottie1" style="height: 200px"></div>
                        <h5 class="mt-2">HTML</h5>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card p-3 text-center shadow">
                        <div id="card-lottie2" style="height: 200px"></div>
                        <h5 class="mt-2">JavaScript
                        </h5>
                    </div>
                </div>
                <div class="col-md-4">
                    <div class="card p-3 text-center shadow">
                        <div
                            id="card-lottie3"
                            style="height: 200px"
                            data-aos="zoom-in"
                        ></div>
                        <h5 class="mt-2">Python</h5>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.skil {
    background-image: url("../assets/skil.jpg");
    background-size: cover;
    background-position: center;
    padding: 60px 0;
    color: white;
}
.card {
    background-color: rgba(255, 255, 255, 0.9);
    border-radius: 30px;
}
</style>
