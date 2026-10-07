<script setup>
import ShowCount from '@/components/ShowCount.vue'
import ResetButton from '@/components/ResetButton.vue'
import { ref } from 'vue'

const count = ref(0)
const onReset = (val) => {
	count.value = val
	return count.value
}
</script>
<template>
	<!-- <ShowCount bar="bar" /> -->
	<ShowCount :foo="count" />
	<button @click="count++">+1</button>
	<ResetButton @reset="count = $event" />
	<ResetButton @reset-count="onReset" />
</template>

<style></style>
