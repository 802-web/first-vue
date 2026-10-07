<script setup>
// const props = defineProps(['foo'])
// console.log(props.foo)

defineProps({
	foo: {
		type: Number,
		required: true,
		validator(val) {
			return val === 0 || val === 1
		}
	}
})
</script>
<template>
	<p>count:{{ foo }}</p>
</template>
