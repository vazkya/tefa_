<template>
  <div class="row p-3 bg-primary text-white align-items-center">
    <!-- Logo SMK -->
    <div class="col-lg-1 text-center">
      <img src="~/assets/img/LOGO-SMK4.webp" alt="Logo SMKN 4" />
    </div>

    <!-- Informasi Perpus -->
    <div class="col-lg-11">
      <h1 class="title">PERPUS DIGITAL</h1>
      <address class="address">
        SMKN 4 Tasikmalaya<br />
        Jl. Depok, Sukamenak, Purbakarta
      </address>
    </div>
  </div>
</template>

<style scoped>
/* Gaya untuk logo */
img {
  margin-top: 5px;
  height: 130px;
  width: 110px;
}

/* Gaya untuk judul */
.title {
  margin-top: 10px;
  margin-left: 10px;
  font-size: 2rem;
  font-weight: bold;
}

/* Gaya untuk alamat */
.address {
  margin-left: 10px;
  font-size: 1rem;
  line-height: 1.5;
}
</style>