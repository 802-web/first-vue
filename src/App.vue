<script setup>
import { ref } from 'vue'
const ok = ref(true)
// const maybeOk = ref(false)
</script>
<template>
	<button @click="ok = !ok">toggle</button>
	<div v-show="ok">
		<p>OK</p>
		<p>maybe OK</p>
		<p>no OK</p>
	</div>
</template>
<style></style>
