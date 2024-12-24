<template>
    <div>
      <!-- Navbar -->
        <nav class="navbar navbar-expand-lg bg-primary navbar-dark" style="margin-bottom: 40px;">
            <div class="container">
            <!-- Logo dan Brand -->
                    <img src="~/assets/img/logo.png" alt="Logo Sekolah" width="30" height="35" class="me-2">
                    <div style="color: white;">SMKN 4 TASIKMALAYA</div>
    
            <!-- Tombol Toggler untuk Mobile -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
    
            <!-- Menu Navbar -->
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item">
                        <nuxt-link class="nav-link" to="./">BERANDA</nuxt-link>
                    </li>
                    <li class="nav-item">
                        <nuxt-link class="nav-link" to="./profil">PROFIL</nuxt-link>
                    </li>
                    <li class="nav-item">
                        <nuxt-link class="nav-link" to="./data">DATA</nuxt-link>
                    </li>
                    <li class="nav-item">
                        <nuxt-link class="nav-link" to="./jurusan">JURUSAN</nuxt-link>
                    </li>
                    <li class="nav-item">
                        <nuxt-link class="nav-link" to="./eskul">EKSTRAKURIKULER</nuxt-link>
                    </li>
                </ul>
            </div>
            </div>
        </nav>
  
        <!-- Konten Halaman -->
        <nuxt />
    </div>
</template>
  
  <script>
  export default {
    name: 'DefaultLayout'
  }
  </script>
  
  <style scoped>
  /* Menambahkan padding pada navbar */
  .navbar {
    padding: 10px 15px;
  }
  
  /* Styling untuk logo */
  .navbar-brand img {
    max-height: 35px;
  }
  </style>