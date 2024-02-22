<script setup>
const { data, error, pending } = await useFetch('https://fakestoreapi.com/products/');
</script>
<template>
  <div v-if="pending">Loading...</div>
  <div v-else-if="error">Error loading data</div>
  <div v-else>{{ data }}</div>
</template>

<style>
.container {
  max-width: 1200px;
  margin: auto;
  padding: 20px;
}
.title {
  text-align: center;
}
.products {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}
.product-card {
  border: 1px solid #eee;
  border-radius: 8px;
  overflow: hidden;
  width: 200px;
  text-align: center;
}
.product-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}
.product-info {
  padding: 10px;
}
</style>
