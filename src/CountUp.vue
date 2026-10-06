<script setup>
import { ref } from 'vue'

const num = ref(0)
</script>
<template>
	<h2>hhh2</h2>
	<p>{{ num }}</p>
	<button @click="num++">up</button>
</template>
