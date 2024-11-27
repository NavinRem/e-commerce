<template>
  <div
    v-for="prom in promotions"
    class="each_promotion nunito"
    :style="{ backgroundColor: prom.bg_color }"
  >
    <div class="content">
      <h3>{{ prom.content }}</h3>
      <Button_Component :prom_content="prom.content" />
    </div>
    <img :src="prom.img" alt="Image" />
  </div>
</template>

<script>
import Button_Component from "./button_component.vue";
import prom_data from "../stores/promotions.json";

export default {
  data() {
    return {
      promotions: prom_data,
    };
  },
  components: {
    Button_Component,
  },
};
</script>

<style scoped>
.each_promotion {
  position: relative;
  color: black;
  display: flex;
  justify-content: end;
  width: 500px;
  height: 200px;
  display: flex;
  border-radius: 10px;
}

.content {
  width: 250px;
  position: absolute;
  left: 40px;
  top: 25px;
  line-height: 30px;
  font-size: 1.3rem;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  height: 150px;
}
.each_promotion img {
  border-radius: 10px;
}
</style>
