<script setup>
import { ref } from 'vue'
const ok = ref(true)
const maybeOk = ref(false)
</script>
<template>
	<button @click="ok = !ok">toggle</button>
	<template v-if="ok">
		<p>OK</p>
		<p>maybe OK</p>
		<p>no OK</p>
	</template>
</template>
<style></style>
