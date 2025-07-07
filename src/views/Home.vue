<script setup>
import { onMounted } from "vue";
import lottie from "lottie-web";
import animationData from "../assets/bumi.json";

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
    <html class="bg-anu">
        <header class="text-center py-5" data-aos="zoom-in">
            <div class="container">
                <div class="d-flex justify-content-end align-items-end g-4">
                    <!-- kolom teks -->
                    <div class="col-md-6">
                        <h1 class="ha1 display-5 fw-bold" data-aos="fade-down">
                            Welcome Guys!
                        </h1>
                        <p class="ha1 mt-5" data-aos="fade-up">
                            Halo! Nama saya <b>Nur Syafii </b>, dan saya seorang
                            IT Developer yang memiliki hasrat mendalam terhadap
                            teknologi dan pengembangan perangkat lunak. Sejak
                            awal saya tertarik dengan dunia pemrograman, saya
                            telah berkomitmen untuk terus belajar, berinovasi,
                            dan memberikan solusi teknologi yang dapat
                            mempermudah kehidupan serta meningkatkan efisiensi.
                        </p>
                    </div>
                    <!-- kolom animasi -->
                    <div class="col-md-5 text-center">
                        <div
                            id="lottie"
                            style="max-width: 600px; margin: auto"
                        ></div>
                    </div>
                </div>
                <hr class="my-5" />
            </div>
        </header>
    </html>
</template>

<style>
.bg-anu {
    background-image: url("../assets/skil.jpg") !important;
    background-size: 100%;
}
.ha1 {
    color: white;
    font-family: "poppins";
    font-weight: 300;
}

hr {
    height: 4px;
    background-color: #ffffff;
    margin: 16px 0;
    border-radius: 50px;
    margin-top: 50px;
}
</style>
