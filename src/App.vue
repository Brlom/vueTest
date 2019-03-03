<template>
  <div id="app">
    <!-- <Banner/> -->
    <div id="nav">
      <router-link to="/"></router-link>
      <!-- <router-link to="/">Home&nbsp;</router-link>| -->
      <!-- <router-link to="/about">&nbsp;About&nbsp;</router-link>|
      <router-link to="/articles">&nbsp;Articles</router-link> -->
    </div>
    <router-view/>
  </div>
</template>

<script>
// @ is an alias to /src
import Banner from "@/components/Banner.vue";

export default {
  name: "app",
  components: {
    Banner, 
  }
};
</script>


<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  width: 300px;
  flex-direction: column;
  justify-content: center;
  /* align-items: flex-start; */
  /* align-content: flex-start; */

}
</style>
