<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <h2 class="text-center my-4">BUKU</h2>
                <nuxt-link to="../"><button type="submit" class="btn btn-lg rounded-5 px-5 bg-secondary text-white" style="float: right; margin-bottom: 15px;">KEMBALI</button></nuxt-link>
                <div class="my-3">
                    <form @submit.prevent="getBooks"> 
                        <input v-model="keyword" type="search" class="form-control rounded-5" placeholder="Mau baca apa hari ini?">
                    </form>
                </div>
                <div class="my-3 text-muted">menampilkan 3 dari 3</div>
                <div class="row">
                        <div v-for="(book, i) in books" :key="i" class="col-lg-2"></div>
                        <div class="card mb-3">
                            <img :src="books.cover" class="cover" alt="cover">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const supabase = useSupabaseClient()
const books = ref ([])

onMounted(() => {
    getBooks()
})

const keyword = ref('')

const getBooks = async () => {
    const {data, error} = await supabase.from('buku').select(`*, kategori`)
    .ilike('judul', `%${keyword.value}%`)
    if(data) books.value = data
}
</script>

<style scoped>
.card-body {
    width: 100%;
    height: 20em;
    padding: 0;
}
.cover {
    width: 100%;
    height: 20em;
    object-fit: cover;
    object-position: 0 30;
}
</style>