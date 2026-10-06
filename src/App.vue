<script setup>
import { ref } from 'vue'
const ok = ref(true)
const fruits = ref([
	{ id: 1, name: 'apple' },
	{ id: 2, name: 'orage' },
	{ id: 3, name: 'grape' },
	{ id: 4, name: 'apple2' }
])

const user = {
	name: 'uuu',
	age: 33,
	region: 'america'
}
</script>
<template>
	<!-- <button @click="ok = !ok">toggle</button>
	<div v-show="ok">
		<p>OK</p>
		<p>maybe OK</p>
		<p>no OK</p>
	</div>
	<button @click="fruits.shift()">delete</button>
	<template v-for="({ id, name }, index) in fruits" :key="id">
		<template v-if="id === 2">
			<p>id: {{ id }}</p>
			<input type="text" />{{ name }}({{ index }})
		</template>
	</template> -->

	<p v-for="(val, key, index) in user" :key="val">{{ key }}: {{ val }}({{ index }})</p>

	<p>in versin</p>
	<p v-for="n in 5" :key="n">{{ n }}</p>
	<p>of versin</p>
	<p v-for="n of 5" :key="n">{{ n }}</p>
</template>
<style></style>
