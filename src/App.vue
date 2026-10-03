<script setup>
const title = 'hello vue'
let price = 4
function incremnet() {
	price++
	console.log(price)
}
</script>
<template>
	<h1>Title: {{ title }}</h1>
	<h2>price: {{ price - 1 }}</h2>
	<button @click="incremnet">button</button>
</template>
<style>
h1 {
	color: red;
}
</style>
