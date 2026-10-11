<script setup>
import { ref } from 'vue'

const pageNum = ref(1)
</script>
<template>
	<div>
		<button @click="pageNum = 1">1</button>
		<button @click="pageNum = 2">2</button>
		<button @click="pageNum = 3">3</button>
		<header>
			<slot name="header" :page-num="pageNum" />
		</header>
		<main>
			<slot name="main" />
		</main>
		<footer>
			<slot name="footer">
				<p>kkk</p>
			</slot>
			<p>lll</p>
		</footer>
		<slot />
	</div>

	<!-- <div>
		<slot>
			<p>dounaru?</p>
		</slot>
	</div> -->
</template>
<style scoped>
div {
	padding: 16px;
	box-shadow: 2px 2px 6px rgba(0, 0, 0, 4);
	border-radius: 5px;
	text-align: center;
}
</style>
