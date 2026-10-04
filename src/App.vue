<script setup>
import { computed, ref, watchEffect } from 'vue'

const message = ref('<h1>Hello</h1>')
const url = ref('https://vuejs.org')
const vueId = ref('vue-id')
const count = ref(0)
const countUp = (event, times) => {
	count.value = event.clientX * times
	count.value++
}
const eventName = 'keyup'

const userInput = ref('')

const num = ref(0)
const evaluation = computed(() => {
	return num.value > 5 ? 'good' : 'bad'
})

// watchEffect
const wNum = ref(0)
watchEffect(() => {
	console.log('watchEffect')
	// console.log(wNum.value)
	console.log('ggg')
})
</script>
<template>
	<div v-html="message"></div>
	<a v-bind="{ id: vueId, href: url }">vue</a>
	<p>{{ count }}</p>
	<button @click="count = $event.clientX">button</button>
	<button @click="countUp($event, 5)">countUp</button>
	<div @click="countUp">
		<button @click.stop="">stopPropagation</button>
	</div>
	<a href="https://vuejs.org" @click.prevent="">vue.js</a>
	<input type="text" @keyup.space="count++" />
	<input type="text" @[eventName].delete="count++" />
	<br /><br />

	<p>{{ userInput }}</p>
	<input v-model="userInput" type="text" />
	<br /><br />

	<p>{{ evaluation }}</p>
	<p>{{ num }}</p>
	<button @click="num++">num</button>

	<br /><br />

	<p>{{ wNum }}</p>
	<button @click="wNum++">wNum</button>
</template>
