<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <Calculete msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import Calculete from "@/components/Calculete.vue";

export default {
  name: "Calc",
  components: {
    Calculete,
  },
};
</script>
