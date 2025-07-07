<script setup>
import { onMounted } from "vue";
import lottie from "lottie-web";
import animationData from "../assets/porto.json";

onMounted(() => {
    lottie.loadAnimation({
        container: document.getElementById("lottie"),
        renderer: "svg",
        loop: true,
        autoplay: true,
        animationData: animationData,
    });
});
</script>

<template>
    <div class="me">
        <div class="container">
            <div class="row align-items-center g-4">
                <!-- kolom teks -->
                <div class="col-md-12">
                    <h1
                        class="display-5 fw-bold"
                        style="text-align: left; color: white; margin-top: 40px"
                        data-aos="fade-down"
                    >
                        Portofolio
                    </h1>
                </div>
                <div
                    class="col-md-6 text-center"
                    style="margin-top: 70px; margin-bottom: 40px"
                >
                    <div
                        id="lottie"
                        style="max-width: 300px; margin: auto"
                        data-aos="zoom-in"
                    ></div>
                </div>
                <div class="col-md-6">
                    <p class="ha1" style="text-align: left" data-aos="fade-up">
                        Hallo Guys👋🏻 Selamat datang di Portofolio saya. Berikut
                        adalah beberapa proyek yang pernah saya kerjakan sebagai
                        bagian dari perjalanan saya di dunia software developing
                        dan teknologi informasi. Proyek-proyek ini mencerminkan
                        keahlian saya dalam membangun aplikasi mobile, website,
                        hingga dashboard data.
                    </p>
                </div>
            </div>
            <div class="d-flex  gap-5 justify-content-center align-center">
                <div class="card bg-drak" style="height: 100%; max-width: 350px;">
                    <img class="card-img-top" src="../assets/splash.png" alt="Card image cap" style="border-top-right-radius: 30px; border-top-left-radius: 30px;"/>
                    <div class="card-body">
                        <p class="card-text text-white">
                            Ini adalah salah satu aplikasi yang pernah saya buat. Saya membuat aplikasi ini menggunakan android studio dan flutter.
                        </p>
                    </div>
                </div>
                <div class="card bg-drak" style="height: 100%; max-width: 350px;" >
                    <img class="card-img-top" src="../assets/ingfo.png" alt="Card image cap"style="border-top-right-radius: 30px; border-top-left-radius: 30px;" />
                    <div class="card-body">
                        <p class="card-text text-white">
                            Ini adalah salah satu aplikasi yang pernah saya buat. Saya membuat aplikasi ini menggunakan android studio dan flutter.
                        </p>
                    </div>
                </div>
                <div class="card bg-drak" style="height: 100%; max-width: 350px;" >
                    <img class="card-img-top" src="../assets/gol.png" alt="Card image cap" style="border-top-right-radius: 30px; border-top-left-radius: 30px;" />
                    <div class="card-body">
                        <p class="card-text text-white">
                            Ini merupakan aplikasi yang saya buat. Saya menggunakan bahasa pemrograman css dan sql sebagai databasenya
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.me {
    background-image: url("../assets/anu.jpg");
    background-size: 100%;
}

.goal {
    width: 100px;
}

.bg-drak {
    background-color: rgb(21, 22, 49)!important;
}

.card {
    border-radius: 30px;
}
</style>
