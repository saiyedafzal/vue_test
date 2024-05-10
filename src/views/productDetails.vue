<script setup lang="ts">
import { onBeforeMount, ref } from 'vue';
import { useRoute } from 'vue-router'
const product = ref()
const route = useRoute()
const id = route.params.id

onBeforeMount(async () => {

  const res = await fetch(`https://dummyapi.online/api/products/${id}`)
  product.value = await res.json()
})
</script>

<template>
  <div class="wrapper">
    <div class="product-container">
      <div className="product">
        <h1>{{ product.name }}</h1>
        <img
            :src="product.featuredImage"
            alt={product.name}
            width={800}
            height={600}
            priority
          /> 
        <p>{{product.description}}</p>
      </div>
    </div>
  </div>
</template>

<style>
.product-container {
  display: flex;
  padding: 0 20px;
  flex-wrap: wrap;
  row-gap: 10px;
  column-gap: 10px;
  align-items: center;
  justify-content: center;
  margin-top: 80px;
}
</style>
