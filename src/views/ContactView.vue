<template>
  <div class="contact pt-5">
    <div class="row text-center mb-3">
      <div class="col">
        <h2>Contact</h2>
      </div>
    </div>
    <div class="row justify-content-center">
      <div class="col-md-6">
        <form>
          <div class="form-group mb-3">
            <label for="name" class="form-label">Nama </label>
            <input type="text" class="form-control bg-light" id="name" aria-describedby="name" placeholder="masukkan nama anda" v-model="form.name" />
          </div>
          <div class="form-group mb-3">
            <label for="email" class="form-label">Email </label>
            <input type="email" class="form-control bg-light" id="email" aria-describedby="email" placeholder="masukkan email anda" v-model="form.email" />
          </div>
          <div class="form-group mb-3">
            <label for="pesan" class="form-label">Pesan</label>
            <textarea class="form-control bg-light" id="pesan" rows="3" placeholder="masukkan pesan anda" v-model="form.pesan"></textarea>
          </div>
          <button type="submit" class="btn btn-primary mb-4" @click.privent="inputData">Kirim</button>
        </form>

        <hr />
        <table class="table text-center bg-light">
          <thead>
            <tr>
              <th>Nama</th>
              <th>Email</th>
              <th>Pesan</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="item in data" :key="item.id">
              <td>{{ item.name }}</td>
              <td>{{ item.email }}</td>
              <td>{{ item.pesan }}</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: "",
        email: "",
        pesan: "",
      },
      data: [],
      id: 0,
    };
  },
  methods: {
    inputData() {
      this.data.push({
        id: this.id++,
        name: this.form.name,
        email: this.form.email,
        pesan: this.form.pesan,
      });

      this.form.email = "";
      this.form.name = "";
      this.form.pesan = "";
    },
  },
};
</script>

<style>
.contact {
  margin: 0;
  padding: 15px;
  padding-bottom: 250px;
}

h2 {
  padding-top: 20px;
}
</style>
