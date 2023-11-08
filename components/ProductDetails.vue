<template>
	<div>
		<p>Product details for {{ data?.id }}</p>
		<p>{{ data?.price }} $</p>
		<p>{{ data?.title }}</p>
		<p>
			{{ data?.description }}
		</p>
	</div>
</template>

<script setup lang="ts">
import type { Product } from "~/interfaces/Product";

defineProps({
	data: {
		type: Object as PropType<Product>,
	},
});
</script>

<style scoped></style>
