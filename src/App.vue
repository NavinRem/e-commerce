<script setup>
import category from "./components/category_component.vue";
import promotion from "./components/promotion_component.vue";
</script>

<template>
  <div id="app" class="nunito">
    <div class="cate_container">
      <category />
    </div>
    <br />
    <div class="prom_container">
      <promotion />
    </div>
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200..1000;1,200..1000&display=swap");

.nunito {
  font-family: "Nunito", sans-serif;
  font-optical-sizing: auto;
  font-weight: 900;
  font-style: normal;
}
#app {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
.cate_container {
  width: 1600px;
  padding: 10px;
  display: flex;
  justify-content: space-around;
}
.prom_container {
  width: 1600px;
  padding: 10px;
  display: flex;
  justify-content: space-around;
}
</style>
