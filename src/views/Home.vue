<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <NewVue msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Banner from "@/components/Banner.vue";
import NewVue from "@/components/NewVue.vue";

export default {
  name: "home",
  components: {
    Banner, 
    NewVue
  }
};
</script>
