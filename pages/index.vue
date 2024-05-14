<template>
    <html lang="en">
    <head>
        <meta charset="UT-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>menu</title>
    </head>
    <body>
    <div class="container-fluid">
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

    

            <div class="col-lg-6">
                <nuxt-link to ="/buku">
                    <div class="card bg-buku rounded-5">
                        <div class="card-body">
                            <h2> Cari Buku</h2>
                        </div>
                    </div>
                </nuxt-link>
            </div>
        </div>
    </div>

    <h1 class="statistik">STATISTIK</h1>

        <div class="row my-5">
            <div class="col-lg-6">
                <nuxt-link to="/pengunjung/">
                    <div class="card bg-warning rounded-5">
                        <div class="card-body">
                            <h2 class="font"> {{ jumlahpengunjung }} Pengunjung</h2>
                        </div>
                    </div>
                </nuxt-link>
            </div>

    

            <div class="col-lg-6">
                <nuxt-link to ="/buku">
                    <div class="card bg-success  rounded-5">
                        <div class="card-body">
                            <h1 class="font"> {{jumlahbuku}} Buku</h1>
                        </div>
                    </div>
                </nuxt-link>
            </div>
        </div>
        <div>
                <Chart />
            </div>
    </body>
    </html>
</template>

<script setup>
const supabase = useSupabaseClient()
const jumlahpengunjung = ref (0)
const jumlahbuku = ref (0)

async function ambiljumlahpengunjung() {
    const { data,error, count} = await supabase
    .from("pengunjung")
    .select("*", {count: 'exact'});
    if (count) jumlahpengunjung.value = count;
}
async function ambiljumlahbuku() {
    const { data,error, count} = await supabase
    .from("buku")
    .select("*", {count: 'exact'});
    if (count) jumlahbuku.value = count;
}


onMounted(() => {
    ambiljumlahpengunjung();
    ambiljumlahbuku();
})
</script>

<style scoped>
.card {
    height: 250px;
    margin-right: 27px;
    box-shadow: 3px 1px 10px #424242;
}
.card.bg-pengunjung {
    margin-top: 5%;
    background-image: url('../assets/img/bg-home-kunjungan.jpeg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
    opacity: 90%;
}
.card.bg-buku {
    margin-top: 5%;
    background-image: url('../assets/img/bg-home-cari-buku.jpg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
    opacity: 90%;
}
h2{
   color: black;
   font: arial;
}
h1{
    color: white;
}
.card.bg-success {
    margin-top: 2%;
}

.card.bg-warning {
    margin-top: 2%;
}
.statistik {
    color: black;
    margin-left: 50px;
}
.font{
    text-align: center;
    margin-top: 80px;
    font-size: 250%;
    color: black;
}
</style>