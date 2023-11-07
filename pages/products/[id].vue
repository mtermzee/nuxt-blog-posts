<template>
	<div class="flex flex-col w-4/5 m-auto justify-center items-start">
		<p>Product details for {{ id }}</p>
		<p>
			Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti
			perferendis ipsa quae non incidunt, officia dolor ducimus hic corporis.
			Repudiandae.
		</p>
	</div>
</template>

<script setup>
const { id } = useRoute().params;
</script>

<style scoped></style>
