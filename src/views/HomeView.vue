<template>
  <!-- Jumbotron -->
  <div class="home">
    <div class="row text-center pt-5 mx-auto my-auto">
      <div class="col">
        <img alt="Vue logo" src="../assets/foto.png" width="150" class="rounded-circle img-thumbnail mt-5" />
        <h1>Nurul Ikhsan</h1>
        <p class="lead">Informatics Engineering student at UIN SUSKA RIAU</p>
      </div>
    </div>
  </div>
  <!-- Akhir Jumbotron -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
  },
};
</script>

<style>
.home {
  margin: 0;
  padding: 0;
  background-color: #e2edff;
  padding-bottom: 345px;
}
</style>
