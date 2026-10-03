<script setup>
import { ref } from 'vue'

const message = ref('<h1>Hello</h1>')
const url = ref('https://vuejs.org')
const vueId = ref('vue-id')
</script>
<template>
	<div v-html="message"></div>
	<a v-bind="{ id: vueId, href: url }">vue</a>
</template>
