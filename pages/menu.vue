<template>
  <div class="container body">
    <Css />
    <Navigasi />
    <Product />
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: "",
    };
  },
  mounted() {
    this.ambilData();
  },
  methods: {
    async ambilData() {
      const { data, error } = await this.$supabase.from("tb_produk").select();
      if (data) this.items = data;
      if (error) console.log(error);
    },
  },
};
</script>
