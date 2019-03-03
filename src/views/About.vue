<template>
  <div id="example-1">
  <br/>
  <button @click="show = !show">
    Toggle render
  </button>
  <transition name="slide-fade">
    <p v-if="show">hello</p>
  </transition>
</div>
</template>

<script>
export default {
  el: "#example-1",
  data: {
    show: true
  }
};
</script>