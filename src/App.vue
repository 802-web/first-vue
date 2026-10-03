<script setup>
import { reactive, ref } from 'vue'
const title = 'hello vue'
let price = ref(4)
function incremnet() {
	price.value++
	instructor.age++
	instructor.bio = 'ushishi'
	instructor.sns.instagram = 'tkk'
	instructor.email = 'emal'
}
let info = ref({
	student: 'uuu',
	age: 2
})
const instructor = reactive({
	name: 'mowmow',
	age: 3,
	sns: {
		twitter: 'twitter',
		instagram: 'insta'
	},
	email: ref('kkk@.com')
})
instructor.bio = 'hello'

const option = {
	key: ref('ww'),
	val: ref(3)
}
console.log(option.key)
</script>
<template>
	<h1>Title: {{ title }}</h1>
	<h2>price: {{ price }}</h2>
	<h2>student: {{ info.age }}</h2>
	<h2>instructor: {{ instructor.age }}</h2>
	<h2>instructor bio: {{ instructor.bio }}</h2>
	<h2>instructor sns: {{ instructor.sns.instagram }}</h2>
	<h2>instructor email: {{ instructor.email }}</h2>
	<h2>option: {{ option.val.value + 1 }}</h2>
	<button @click="incremnet">button</button>
</template>
<style>
h1 {
	color: red;
}
</style>
