<template>
  <div class="articles">
    <h1>This is an articles page</h1>
    <NewVue></NewVue>
  </div>
</template>

<script>
// @ is an alias to /src
import NewVue from "@/components/NewVue.vue";

export default {
  name: "articles",
  components: {
    NewVue
  }
};
</script>