<script>
import category from "./components/category_component.vue";
import button from "./components/button_component.vue";
import promotion from "./components/promotion_component.vue";

export default {
  components: {
    category,
    button,
    promotion,
  },
  data() {
    return {
      category: [],
      promotion: [],
      button: [],
    };
  },
};
</script>

<template>
  <div id="app">
    <category> </category>
    <promotion> </promotion>
    <button></button>
  </div>
  <RouterView />
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: black;
}
body {
  background-color: aliceblue;
}
</style>
