<template>
  <div class="container body">
    <Navigasi class="mb-5" />
    <!-- contact -->
    <section class="contact" id="contact">
      <div class="container">
        <div class="row">
          <div class="col-sm-12 text-center">
            <h2>Contact</h2>
            <hr />
          </div>
        </div>

        <div class="row">
          <div class="col-sm-8 col-sm-offset-2">
            <form action="">
              <div class="form-group">
                <label for="nama">Name</label>
                <input
                  type="text"
                  id="nama"
                  class="form-control"
                  placeholder="Full Name"
                />
              </div>
              <div class="form-group">
                <label for="email">Email</label>
                <input
                  type="email"
                  id="email"
                  class="form-control"
                  placeholder="email@gmail.com"
                />
              </div>
              <div class="form-group">
                <label for="telp">No Telp</label>
                <input
                  type="tel"
                  id="telp"
                  class="form-control"
                  placeholder="08xxxxxxxxxx"
                />
              </div>
              <div class="form-group">
                <label for="pesan">Message</label>
                <textarea
                  class="form-control"
                  rows="10"
                  placeholder="Enter your massage"
                ></textarea>
              </div>
              <button type="submit" class="btn btn-primary btn-md ">Submit </button>
              </button>
            </form>
          </div>
        </div>
      </div>
    </section>
    <!-- akhir contact -->
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      nohp: "",
      massage: "",
    };
  },
  mounted() {
    this.isiData();
  },
  methods: {
    async isiData() {
      const { data, error } = await this.$supabase.from("contact").insert();
      if (data) {
        this.datas = data;
      }
      if (error) console.log(error);
    },
  },
};
</script>
