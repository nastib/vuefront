<template>
  <span>
    <p>JSON DATA !!!: </p>
    <ul>
      <li v-for="product in jsonData" :key="product.id" style="list-style-type: none;">
     <b>Name:</b> {{ product.title }}, <br> <p><b>Price: $</b> {{ product.price }}</p>, 
    <p> <b>Photo</b></p> <img :src="product.image" alt="Photo" style="  height: 100px;
     width: 100px;">
      </li>
    </ul>
  </span>
</template>

<script setup lang="ts">import { onMounted, ref } from 'vue';
const jsonData = ref()
onMounted(async () => {
  const response = await fetch('https://fakestoreapi.com/products?limit=5')
  jsonData.value = await response.json();
   
  }
);
</script>
<style scoped>
span {
  font-size: 1.2em;
  text-align: center;
}
</style>
