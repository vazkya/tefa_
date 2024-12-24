<template>
    <div id="jurusan" class="container mt-5">
        <div class="row">
            <div class="col text-center">
            <h2>Jurusan</h2>
            <p>Berbagai jurusan menarik yang tersedia di SMKN 4 Tasikmalaya.</p>
            </div>
        </div>
    
        <!-- Row Card Jurusan -->
        <div class="row mt-4">
            <!-- Card TKJ -->
            <div class="col-md-4 mb-4">
            <div class="shadow card h-100">
                <div class="card-body text-center bg-primary" style="color: white;">
                <h5 class="card-title">Teknik Komputer dan Jaringan (TKJ)</h5>
                <p class="card-text">Mahir dalam jaringan komputer dan teknologi informasi.</p>
                <p class="card-text"><strong>Jumlah Murid: 120</strong></p>
                </div>
            </div>
            </div>
    
            <!-- Card RPL -->
            <div class="col-md-4 mb-4">
            <div class="shadow card h-100">
                <div class="card-body text-center bg-success" style="color: white;">
                <img src="~/assets/img/rpl.png" alt="Logo Sekolah" width="30" height="35" class="me-2">
                <h5 class="card-title">Rekayasa Perangkat Lunak (RPL)</h5>
                <p class="card-text">Ahli dalam pengembangan perangkat lunak modern.</p>
                <p class="card-text"><strong>Jumlah Murid: 100</strong></p>
                </div>
            </div>
            </div>
    
            <!-- Card DKV -->
            <div class="col-md-4 mb-4">
            <div class="shadow card h-100">
                <div class="card-body text-center bg-warning" style="color: white;">
                <h5 class="card-title">Desain Komunikasi Visual (DKV)</h5>
                <p class="card-text">Kreatif dalam seni desain dan komunikasi visual.</p>
                <p class="card-text"><strong>Jumlah Murid: 90</strong></p>
                </div>
            </div>
            </div>
    
            <!-- Card TBSM -->
            <div class="col-md-6 mb-4">
            <div class="shadow card h-100">
                <div class="card-body text-center bg-danger" style="color: white;">
                <h5 class="card-title">Teknik Bisnis Sepeda Motor (TBSM)</h5>
                <p class="card-text">Ahli dalam perbaikan dan manajemen bisnis sepeda motor.</p>
                <p class="card-text"><strong>Jumlah Murid: 80</strong></p>
                </div>
            </div>
            </div>
    
            <!-- Card TOI -->
            <div class="col-md-6 mb-4">
            <div class="shadow card h-100">
                <div class="card-body text-center bg-secondary" style="color: white;">
                <h5 class="card-title">Teknik Otomasi Industri (TOI)</h5>
                <p class="card-text">Mahir dalam sistem otomatisasi dan teknologi industri.</p>
                <p class="card-text"><strong>Jumlah Murid: 70</strong></p>
                </div>
            </div>
            </div>
        </div>
    </div>
</template>
  
  <script>
  export default {
    data() {
      return {
        jurusan: [
          { name: "Teknik Komputer dan Jaringan (TKJ)", description: "Mahir dalam jaringan komputer dan teknologi informasi.", students: 120 },
          { name: "Rekayasa Perangkat Lunak (RPL)", description: "Ahli dalam pengembangan perangkat lunak modern.", students: 100 },
          { name: "Desain Komunikasi Visual (DKV)", description: "Kreatif dalam seni desain dan komunikasi visual.", students: 90 },
          { name: "Teknik Bisnis Sepeda Motor (TBSM)", description: "Ahli dalam perbaikan dan manajemen bisnis sepeda motor.", students: 80 },
          { name: "Teknik Otomasi Industri (TOI)", description: "Mahir dalam sistem otomatisasi dan teknologi industri.", students: 70 }
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  .card {
    border-radius: 10px;
  }
  </style>