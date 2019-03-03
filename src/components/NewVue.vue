<template>
  <div id="app">
    <!-- <p>Created a new component using Vue.js!</p>
    <button v-on:click="addToCount()">Add 1</button>
    <p>The button above has been clicked {{counter}} times</p>-->
    <div>
      <img alt="Ancorman" src="../assets/bg.jpg">
    </div>
    <div>
      <h1>
        <i class="fab fa-twitter"></i>HAVE YOUR SAY!
      </h1>
    </div>
    <div class="speech-bubble-box">
      <div
        class="speech-bubble sb1"
      >"LOREM IPSUM DOLOR SIT AMET, CONSECTETUR ADIPISCING ELIT, SED DO EIUSMOD TEMPOR INCIDIDUNT UT LABORE ET DOLORE MAGNA ALIQUA.QUIS IPSUM"</div>
    </div>
    <!-- <div v-for="article in articles">{{ article.title }}</div> -->
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "NewVue",
  props: {
    msg: String
  },
  data() {
    return {
      counter: 0,
      articles: []
    };
  },
  methods: {
    addToCount() {
      this.counter += 1;
    }
  },
  mounted() {
    axios
      .get("https://my-nc-knews.herokuapp.com/api/articles")
      .then(response => (this.articles = response.data.articles));
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "https://use.fontawesome.com/releases/v5.7.2/css/all.css";
@import "https://use.typekit.net/pmz0fjm.css";

#app {
  font-family: "Bebas Neue";
  /* order: 1; 
  flex-basis: 20% | auto;  
  width: 200px;
  height: 20px; */
}

/* div {
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  color: #223344;
} */

i {
  padding: 0px 16px;
  font-size: 30px;
}

h1 {
  /* background-color: #e819b4; */
  background-image: linear-gradient(to right, pink, orange);
  color: #ffffff;
  padding-top: 15px;
  padding-right: 5px;
  padding-bottom: none;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  font-size: 22px;
  order: 1;
  flex-basis: 18% | auto;
  width: 255px;
  height: 40px;
  position: absolute;
  bottom: 550px;
}

.speech-bubble-box {
  /* TODO: need to figure out how to move*/
  order: 2;
  z-index: 2;
  background-color: #000000;
  width: 500px;
  height: 100px;
}

.speech-bubble {
  width: 437px;
  margin: 50px 16px;
  background: #ffffff;
  padding: 15px;
  text-align: center;
  font-weight: 900;
  font-size: 10px;
  color: #000000;
  font-family: arial;
  position: relative;
  top: 265px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
}

.sb1:before {
  content: "";
  width: 0px;
  height: 0px;
  position: absolute;
  border-left: 10px solid #ffffff;
  border-right: 10px solid transparent;
  border-top: 10px solid #ffffff;
  border-bottom: 10px solid transparent;
  left: 0px;
  bottom: -19px;
}

img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
  width: 70%;
  height: 70%;
}
</style>