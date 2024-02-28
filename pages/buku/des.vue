<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <div class="row">
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="~/assets/img/cover.jpg" class="cover" alt="cover 1">
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-7">
                        <h3>JUDUL : EPISODE HUJAN</h3><br>
                        <p>PENULIS : Lucia Priandarini</p>
                        <P>PENERBIT : GRAMEDIA WIDIASARANA INDONESIA</P>
                        <p>TAHUN TERBIT : (15 OKTOBER 2022)</p>
                        <p>JUMLAH HALAMAN : 292</p>
                        <p>DESKRIPSI : Buku novel romantis ini sangat menarik untuk dibaca oleh remaja yang sedang kasmaran, memiliki pembahasan dan cerita yang menarik dan banyak kata-kata puitis yang tertuang di buku ini seperti: “Hujan membuatku merasa tidak sendiri. Rintik hujan membuatku sadar. Aku bukan satu-satunya orang yang jatuh, lalu pecah membentur batu dan aspal jalanan, atau larut bersama kelokan sungai.” “Pluviophile,” ucap Katya. “Apa itu?” “Itu kamu. Orang yang merasakan kedamaian saat hujan,” ungkap Katya. Meski ia tahu, pria itu “Banyu Mili” sepertinya bisa merasa damai kapanpun juga. Bagi orang lain, pembicaraan tentang hujan barangkali terdengar konyol.</p>
                    </div>
                </div>
                <div>
                    <nuxt-link to="../"><button type="submit" class="btn btn-lg rounded-5 px-5 bg-secondary text-white" style="float: right; margin-top: 15px;">KEMBALI</button></nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.cover {
    height: 300px;
    width: 200px;
}
.card.mb-3 {
    margin-top: 50px;
    margin-left: 20px;
    height: 340px;
    width: 235px;
}
h3{
    margin-top: 50px;
    margin-left: 20px;
    margin-bottom: 1px;
}
p {
    margin-left: 20px;
    margin-bottom: 7px;
}
</style>