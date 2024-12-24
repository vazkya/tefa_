<template>
    <div class="container mt-4">
      <!-- Konten Profil Sekolah -->
        <div class="d-flex align-items-center flex-wrap">
            <!-- Kolom Tabel Informasi -->
            <div class="p-2 flex-fill">
            <h2>Informasi Sekolah</h2>
            <table class="table table-bordered">
                <tbody>
                <tr>
                    <th scope="row">Nama Sekolah</th>
                    <td>SMKN 4 Tasikmalaya</td>
                </tr>
                <tr>
                    <th scope="row">Tahun Berdiri</th>
                    <td>1985</td>
                </tr>
                <tr>
                    <th scope="row">Alamat</th>
                    <td>Jl. Contoh Alamat No. 123, Tasikmalaya</td>
                </tr>
                <tr>
                    <th scope="row">Visi</th>
                    <td>Terwujudnya lulusan yang cerdas, aktif, dan kompetitif</td>
                </tr>
                </tbody>
            </table>
            </div>
    
            <!-- Kolom Gambar Logo -->
            <div class="p-2 flex-fill text-center">
            <img src="~/assets/img/logo.png" alt="Logo SMKN 4 Tasikmalaya" class="img-fluid rounded" 
                style="max-width: 150px; height: auto;">
            </div>
        </div>
        <h3>SEJARAH</h3>
        <p>Sejalan dengan Program Pemerintah dibidang pendidikan Menengah Kejuruan pada saat itu yakni pemerataan akses ditambah pula dengan banyaknya keinginan masyarakat yang mengharapkan adanya SMK Negeri di daerah Kecamatan Purbaratu Kota  Tasikmalaya, terutama untuk menampung tamatan dari SLTP yang ingin melanjutkan ke SMK maka beberapa tokoh masyarakat, unsur pejabat pemerintah di Kecamatan Purbaratu Kota Tasikmalaya mengusulkan kepada pemerintah Kota Tasikmalaya dan Pemerintah Provinsi Jawa Barat, agar berdirinya SMK Negeri di Kecamatan Purbaratu Kota Tasikmalaya.
Setelah melalui perjuangan yang sangat panjang dari berbagai pihak khususnya Disdik Kota Tasikmalaya dan pihak-pihak terkait lainnya sesuai prosedur dan ketentuan yang berlaku pada waktu itu dengan mengucapkan syukur Alhamdulillah akhirnya pada tahun pelajaran 2010/2011 SMK Negeri 4 Tasikmalaya mulai berdiri, pada awalnya membuka Kompetensi Keahlian Teknik Komputer dan Jaringan dengan pendaftar peserta Didik Baru pada waktu itu berjumlah 44 orang. Pada awalnya tempat belajar menumpang di SMP Negeri 17 Kota Tasikmalaya, dan sekolah induknya adalah SMK Negeri 2 Kota Tasikmalaya, Untuk Tenaga pendidik dan Tenaga Kependidikan masih dibantu sepenuhnya oleh kedua sekolah tersebut.
Pada tahun 2012 keluarlah surat Izin Pendirian berdasarkan keputusan kepala Badan Pelayanan Perizinan Terpadu Kota Tasikmalaya No. 420/9/SK-BPPT/2012 Tanggal 06 Februari 2012.</p>
    </div>
</template>
  
<script>
export default {
    name: 'ProfilPage',
}
</script>
  
<style scoped>
h2{
    margin-bottom: 20px;
}
</style>