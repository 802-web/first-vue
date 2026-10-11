<script setup>
import { onActivated, onDeactivated, onMounted, onUnmounted, ref } from 'vue'

const num = ref(0)
onMounted(() => {
	console.log('CompA OnMounted')
})
onUnmounted(() => {
	console.log('CompA UnMounted')
})
onActivated(() => {
	console.log('CompA Activated')
})
onDeactivated(() => {
	console.log('CompA Deactivated')
})
</script>
<template>
	componentA
	<p>{{ num }}</p>
	<button @click="num++">+1</button>
</template>
