<script setup>
import { RouterLink, RouterView } from 'vue-router'
const items = [
  { to: '/',          name: 'Tentang' },
  { to: '/education', name: 'Pendidikan' },
  { to: '/experience',name: 'Pengalaman' },
  { to: '/portfolio', name: 'Portofolio' },
  { to: '/skills',    name: 'Keahlian' },
  { to: '/contact',   name: 'Kontak' }
]
</script>



<template>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg navbar-dark bg-orange sticky-top">
    <div class="container">
      <RouterLink class="navbar-brand" style="font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif" to="/"><strong>Muhammad Nur Syafii</strong></RouterLink>
      <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#nav">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div id="nav" class="collapse navbar-collapse">
        <ul class="navbar-nav ms-auto">
          <li v-for="i in items" :key="i.to" class="nav-item">
            <RouterLink class="nav-link" :to="i.to">{{ i.name }}</RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Transisi halaman -->
  <transition name="fade-page" mode="out-in">
    <RouterView />
  </transition>

  <!-- Footer -->
  <footer class="bg-orange text-center text-white py-3">
    © 2025 Muhammad Nur Syafii
  </footer>
</template>

<style>
.fade-page-enter-active,
.fade-page-leave-active {
  transition: all 0.4s ease;
}
.fade-page-enter-from {
  opacity: 0; transform: translateY(20px);
}
.fade-page-leave-to {
  opacity: 0; transform: translateY(-20px);
}

.bg-orange {
  background-color: rgb(21, 22, 49);
}

</style>