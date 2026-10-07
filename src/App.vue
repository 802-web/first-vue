<script setup>
import ShowCount from '@/components/ShowCount.vue'
import { ref } from 'vue'

const count = ref(0)
</script>
<template>
	<!-- <ShowCount bar="bar" /> -->
	<ShowCount :foo="count" />
	<button @click="count++">+1</button>
</template>

<style></style>
