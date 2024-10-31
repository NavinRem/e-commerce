<script>
import Button_Component from "./button_component.vue";

export default {
  name: "promotion_component",
  props: {
    content: String,
    Image: String,
  },
  components: {
    Button_Component,
  },
};
</script>

<template>
  <article class="each_promotion">
    <div class="content">
      <h3>{{ content }}</h3>
      <Button_Component />
    </div>
    <img :src="Image" alt="d" />
  </article>
</template>

<style>
.each_promotion {
  background-color: lightskyblue;
  display: flex;
  width: 27rem;
  position: relative;
  height: 14rem;
  align-items: center;
  padding-left: 2rem;
  border-radius: 0.25rem;
}
.each_promotion img {
  width: 22rem;
  height: 100%;
  position: absolute;
  right: 0;
}
.content {
  z-index: 1;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  width: 50%;
}
</style>
