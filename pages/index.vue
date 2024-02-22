<script setup>
const { data, error, pending } = await useFetch('https://fakestoreapi.com/products/');
</script>
<template>
  <div v-if="pending">Loading...</div>
  <div v-else-if="error">Error loading data</div>
  <div v-else>{{ data }}</div>
</template>
