<template>
    <div>
      <!-- Konten Data -->
      <div id="data" class="container mt-5">
        <div class="row">
          <div class="col text-center">
            <h2>Data Sekolah</h2>
            <p>Informasi jumlah guru, staf, dan murid di SMKN 4 Tasikmalaya.</p>
          </div>
        </div>
  
        <!-- Tabel Jumlah Guru, Staf, dan Pegawai -->
        <div class="row mt-4">
          <div class="col">
            <h3>Jumlah Guru dan Staf</h3>
            <table class="table table-bordered">
              <thead>
                <tr>
                  <th>Kategori</th>
                  <th>Jumlah</th>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td>Guru</td>
                  <td>{{ jumlahGuru }}</td>
                </tr>
                <tr>
                  <td>Staf Administrasi</td>
                  <td>{{ jumlahStafAdministrasi }}</td>
                </tr>
                <tr>
                  <td>Pegawai Lainnya</td>
                  <td>{{ jumlahPegawaiLainnya }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
  
        <!-- Tabel Jumlah Murid Per Jurusan -->
        <div class="row mt-4">
          <div class="col">
            <h3>Jumlah Murid Per Jurusan</h3>
            <table class="table table-bordered">
              <thead>
                <tr>
                  <th>Jurusan</th>
                  <th>Jumlah Murid</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="(jumlah, jurusan) in jumlahMuridPerJurusan" :key="jurusan">
                  <td>{{ jurusan }}</td>
                  <td>{{ jumlah }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        // Data jumlah guru, staf, dan pegawai
        jumlahGuru: 50,
        jumlahStafAdministrasi: 15,
        jumlahPegawaiLainnya: 10,
  
        // Data jumlah murid per jurusan
        jumlahMuridPerJurusan: {
          "Teknik Informatika": 120,
          "Teknik Mesin": 100,
          "Teknik Elektro": 80,
          "Teknik Otomotif": 90,
          "Teknik Sipil": 70
        }
      };
    }
  };
  </script>
  
  <style scoped>
  /* Optional: Styling tambahan jika diperlukan */
  </style>