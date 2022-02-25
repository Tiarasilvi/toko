<template>
<main>
  <div class="container">
    <navigasi/>
    <div>
      <div class="jumbotron">
        <h2>product</h2>
      </div>
        <div class="row">
          <div class="col-md-12">
            <div v-if="loading" class="text-center">
              sedang memuat ...
            </div>
          </div>
          <div class="col-md-4" v-for="produk in products" :key="produk.id">
            <div class="card mb-3">
              <div class="card-header">
                <img :src="produk.poto" width="100%" height="350"> 
              </div>
              <div class="card-body">
                <h4>{{ produk.nama}}</h4>
                <h4>Rp{{ produk.harga }}</h4>
                <a :href="produk.link_eksternal" class="btn btn-success btn-block">Beli</a>
              </div>
            </div>
          </div>
        </div>
    </div>
  </div>
</main>
</template>

<script>
export default {
  data() {
    return {
      products: '',
      loading: true,
    }
  },
  mounted() {
    this.ambilData()
  },
  methods: {
    async ambilData() {
      const { data, error } = await this.$supabase
        .from('tb_produk')
        .select()
      if(data) {
        this.products = data
        this.loading = false
      }
      if(error) console.log(error)
    }
  }
}
</script>