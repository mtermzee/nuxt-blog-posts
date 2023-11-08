<template>
	<NuxtLayout>
		<div class="mt-7 max-w-sm mx-auto text-center">
			<p>{{ error.statusCode }}</p>
			<p>{{ error.message }}</p>
		</div>
	</NuxtLayout>
</template>

<script setup lang="ts">
defineProps(["error"]);
</script>

<style scoped></style>
