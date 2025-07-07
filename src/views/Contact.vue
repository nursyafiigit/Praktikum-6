<script setup>
import { onMounted } from "vue";
import lottie from "lottie-web";
import animationData from "../assets/contac.json";

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
    <header class="cont bg-dark py-3" data-aos="zoom-in">
        <div class="row">
            <!-- Kiri: Form -->
            <div class="col-md-6">
                <section class="container my-5" data-aos="fade-up">
                    <div class="container contf">
                        <h2 id="text" class="hed mb-4 text-primary text-center">
                            Contact Me
                        </h2>

                        <div class="col-6 mx-auto text-center mb-2">
                            <label for="nama" class="input">Nama </label>
                        </div>
                        <div class="col-10 mx-auto">
                            <input
                                type="text"
                                id="nama"
                                class="input text-dark mb-4"
                            />
                        </div>

                        <div class="col-6 mx-auto text-center mb-2">
                            <label for="email" class="input">Email </label>
                        </div>
                        <div class="col-10 mx-auto">
                            <input
                                type="email"
                                id="email"
                                class="input text-white mb-4"
                            />
                        </div>

                        <div class="col-6 mx-auto text-center mb-2">
                            <label for="pesan" class="input">Pesan </label>
                        </div>
                        <div class="col-10 mx-auto">
                            <textarea
                                name="pesan"
                                id="pesan"
                                class="pesan mb-4"
                            ></textarea>
                        </div>

                        <div class="d-flex justify-content-center mt-5">
                            <button class="butong">Kirim</button>
                        </div>
                    </div>
                </section>
            </div>
            <div
                class="col-md-6 d-flex align-items-center justify-content-center"
            >
                <section>
                    <div
                        id="lottie"
                        style="max-width: 500px; margin: auto"
                        data-aos="zoom-in"
                    ></div>
                </section>
            </div>
        </div>
    </header>
</template>

<style>
.cont {
    background-image: url("../assets/contact.jpg");
    background-size: 100%;
    align-items: center;
}

.contf {
    outline: 2px solid white;
    border-radius: 12px;
    padding: 30px;
    max-width: 500px !important;
    margin: 0 auto;
    background-color: rgba(0, 0, 0, 0.5); /* Tambahan agar form lebih terbaca */
    backdrop-filter: blur(5px);
}

input.input {
    border-radius: 10px;
    text-emphasis-color: black;
    width: 100%;
    height: 35px;
}

label.input {
    margin-top: 10px;
    color: white;
    font-size: 19px;
}

.pesan {
    border-radius: 10px;
    text-emphasis-color: black;
    width: 100%;
}

.butong {
    width: 84%;
    border-radius: 10px;
    height: 50px;
    background-color: rgb(21, 22, 49);
    color: white;
}
</style>
