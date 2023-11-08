<template>
	<div class="flex flex-col w-4/5 m-auto justify-center items-start">
		<h1>Products page</h1>
		<div class="grid grid-cols-4 gap-5">
			<div v-for="p in products" :key="p.id">
				<NuxtLink :to="'/products/' + p.id">{{ p.title }}</NuxtLink>
			</div>
		</div>
	</div>
</template>

<script setup lang="ts">
import type { Product } from "~/interfaces/Product";

const products = ref<Product[]>([]);

const fetchProducts = async () => {
	const res = await fetch("https://fakestoreapi.com/products");
	const data = await res.json();
	products.value = data;
};

onMounted(() => {
	fetchProducts();
});
</script>

<style scoped></style>
