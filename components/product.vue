<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <h1 class="mt-5 text-center mb-5">Menu</h1>
        <div class="row">
          <div class="col-md-12">
            <div class="text-center mt-3em" v-if="loading">
              <img src="../static/assets/load.gif" alt="" width="30%" />
            </div>
          </div>
          <div class="col-md-4" v-for="item in items" :key="item.id">
            <div class="card mb-3">
              <div class="card-header">
                <img :src="item.foto" alt="" width="100%" height="300px" />
              </div>
              <div class="card-body">
                <h4>{{ item.nama }}</h4>
                <h4>Rp.{{ item.harga }}</h4>
                <a :href="item.link_eksternal" class="btn btn-success btn-block"
                  >Pesan Via Whatsapp</a
                >
              </div>
            </div>
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
      items: "",
      loading: true,
    };
  },
  mounted() {
    this.ambilData();
  },
  methods: {
    async ambilData() {
      const { data, error } = await this.$supabase.from("tb_produk").select();
      if (data) {
        this.items = data;
        this.loading = false;
      }
      if (error) console.log(error);
    },
  },
};
</script>
