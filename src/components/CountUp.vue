<script setup>
import { ref } from 'vue'

const num = ref(0)
</script>
<template>
	<h2 v-bind="$attrs">hhh2</h2>
	<BaseIcon />
	<p>{{ num }}</p>
	<button @click="num++">up</button>
</template>
