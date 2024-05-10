<script setup lang="ts">
import { onBeforeMount, ref } from 'vue';
import { RouterLink } from 'vue-router'

const products = ref()
onBeforeMount(async () => {
    const res = await fetch("https://dummyapi.online/api/products")
    products.value = await res.json()
})
</script>

<template>
    <ul class="product-container">
        <li v-for="product in products" :key="product.id">
            <RouterLink :to="`/product/${product.id}`">
                <div>
                    <h1>{{product.name.length > 10 ? product.name.slice(0, 15) + "..." : product.name}}</h1>
                    <img :src="product.thumbnailImage" alt={{product.name}} width={{400}} height={{300}} />
                </div>
            </RouterLink>
        </li>
    </ul>
</template>

<style scoped>
.product-container {
    display: flex;
    padding: 0 20px;
    flex-wrap: wrap;
    row-gap: 10px;
    column-gap: 10px;
    align-items: center;
    justify-content: center;
}
</style>
