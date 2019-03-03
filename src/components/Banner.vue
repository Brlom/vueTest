<template>
  <div>
      <h1>This is the Header for all of the paths!</h1>
  </div>
</template>

<script>
export default {
  name: "Banner",
  props: {
    msg: String
  }
};
</script>

<style scoped>
  div {
    font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
    color: #123123;
  }
</style>