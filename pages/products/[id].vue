<template>
	<div class="flex flex-col w-4/5 m-auto justify-center items-start">
		<ProductDetails :data="product" />
	</div>
</template>

<script setup lang="ts">
import type { Product } from "~/interfaces/Product";

const { id } = useRoute().params;
const product = ref<Product>();

const fetchProduct = async () => {
	const res = await fetch(`https://fakestoreapi.com/products/${id}`);
	const data = await res.json();
	product.value = data;
};

onMounted(() => {
	fetchProduct();
});
</script>

<style scoped></style>
