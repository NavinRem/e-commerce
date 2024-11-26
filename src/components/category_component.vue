<script setup>
defineProps({
  category: {
    type: Object,
  },
  imgUrl: {
    type: String,
    Required: true,
  },
  title: {
    type: String,
    Required: true,
  },
  quantity: {
    type: Number,
    Required: true,
  },
});
</script>

<script>
import cate_data from "../stores/categories.json";

export default {
  data() {
    return {
      categories: cate_data,
    };
  },
};
</script>

<template>
  <div
    v-for="cate in categories"
    class="each_category"
    :style="{ 'background-color': cate.bg_color }"
  >
    <img :src="cate.img" width="100px" />
    <h4 class="title_product">
      {{ cate.title }}
    </h4>
    <span>{{ cate.quantity }} Items</span>
  </div>
</template>

<style>
.each_category {
  width: 8.25rem;
  height: 12rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 0.5rem;
  margin-bottom: 1rem;
  border-radius: 0.45rem;
  gap: 0.05rem;
  box-shadow: 5px 5px 5px rgba(222, 222, 222, 0.1);
  color: black;
  border: none;
}

.each_category:hover {
  border: 1.6px solid #81b13d;
  outline: none;
}

.each_category img {
  width: 6rem;
  height: 6rem;
}

.each_category span {
  font-size: small;
  color: rgb(124, 132, 138);
}

.each_category .title_product {
  margin-top: 0.5rem;
}
</style>
