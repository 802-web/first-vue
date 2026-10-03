<script setup>
import { ref } from 'vue'

const message = ref('<h1>Hello</h1>')
</script>
<template>
	<div v-html="message"></div>
</template>
