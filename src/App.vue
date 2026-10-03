<script setup>
import { ref } from 'vue'
const title = 'hello vue'
let price = ref(4)
function incremnet() {
	price.value++
}
let info = ref({
	student: 'uuu',
	age: 2
})
console.log(info.value.student)
</script>
<template>
	<h1>Title: {{ title }}</h1>
	<h2>price: {{ price - 1 }}</h2>
	<h2>student: {{ info.age }}</h2>
	<button @click="incremnet">button</button>
</template>
<style>
h1 {
	color: red;
}
</style>
