<script setup>
const emit = defineEmits(['resetCount'])

const onReset = () => {
	emit('resetCount', 10)
}
</script>

<template>
	<button @click="onReset">Reset</button>
</template>
