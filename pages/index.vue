<template>
  <div class="container-fluid">
    <!-- Bagian Pengunjung -->
    <div class="row my-5">
      <div class="col-lg-6">
        <nuxt-link to="/pengunjung/tambah">
          <div class="card bg-pengunjung rounded-5">
            <div class="card-body">
              <h2>Pengunjung</h2>
            </div>
          </div>
        </nuxt-link>
      </div>

      <!-- Bagian Cari Buku -->
      <div class="col-lg-6">
        <nuxt-link to="/buku">
          <div class="card bg-buku rounded-5">
            <div class="card-body">
              <h2>Cari Buku</h2>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>

    <!-- Bagian Statistik -->
    <h1 class="statistik">STATISTIK</h1>
    <div class="row my-5">
      <div class="col-lg-6">
        <nuxt-link to="/pengunjung">
          <div class="card bg-warning rounded-5">
            <div class="card-body">
              <h2 class="font">{{ jumlahpengunjung }} Pengunjung</h2>
            </div>
          </div>
        </nuxt-link>
      </div>

      <div class="col-lg-6">
        <nuxt-link to="/buku">
          <div class="card bg-success rounded-5">
            <div class="card-body">
              <h1 class="font">{{ jumlahbuku }} Buku</h1>
            </div>
          </div>
        </nuxt-link>
      </div>
    </div>

    <!-- Komponen Chart -->
    <div>
      <Chart />
    </div>
  </div>
</template>

<script setup>
// Inisialisasi Supabase Client
const supabase = useSupabaseClient();

// State untuk jumlah pengunjung dan jumlah buku
const jumlahpengunjung = ref(0);
const jumlahbuku = ref(0);

// Fungsi untuk mengambil jumlah pengunjung dari Supabase
async function ambilJumlahPengunjung() {
  const { count } = await supabase
    .from('pengunjung')
    .select('*', { count: 'exact' });
  if (count !== null) jumlahpengunjung.value = count;
}

// Fungsi untuk mengambil jumlah buku dari Supabase
async function ambilJumlahBuku() {
  const { count } = await supabase
    .from('buku')
    .select('*', { count: 'exact' });
  if (count !== null) jumlahbuku.value = count;
}

// Ambil data ketika komponen dimuat
onMounted(() => {
  ambilJumlahPengunjung();
  ambilJumlahBuku();
});
</script>

<style scoped>
/* Gaya umum untuk kartu */
.card {
  height: 250px;
  margin-right: 27px;
  box-shadow: 3px 1px 10px #424242;
}

/* Gaya untuk latar belakang kartu Pengunjung */
.card.bg-pengunjung {
  margin-top: 5%;
  background-image: url('../assets/img/bg-home-kunjungan.webp');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  opacity: 0.9;
}

/* Gaya untuk latar belakang kartu Cari Buku */
.card.bg-buku {
  margin-top: 5%;
  background-image: url('../assets/img/bg-home-cari-buku.webp');
  background-repeat: no-repeat;
  background-position: center center;
  background-size: cover;
  opacity: 0.9;
}

/* Gaya untuk statistik */
.card.bg-success,
.card.bg-warning {
  margin-top: 2%;
}

.statistik {
  margin-left: 50px;
  color: black;
}

.font {
  text-align: center;
  margin-top: 80px;
  font-size: 250%;
  color: black;
}

h2 {
  color: black;
  font-family: Arial, sans-serif;
}

h1 {
  color: white;
}
</style>