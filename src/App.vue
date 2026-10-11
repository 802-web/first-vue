<script setup>
import ShowCount from '@/components/ShowCount.vue'
import ResetButton from '@/components/ResetButton.vue'
import BaseCard from '@/components/BaseCard.vue'
import { ref } from 'vue'

const count = ref(0)
const onReset = (val) => {
	count.value = val
	return count.value
}
</script>
<template>
	<!-- <ShowCount bar="bar" /> -->
	<!-- <ShowCount :foo="count" />
	<button @click="count++">+1</button>
	<ResetButton @reset="count = $event" />
	<ResetButton @reset-count="onReset" /> -->

	<div>Slots</div>
	<BaseCard>
		<!-- <h2>h3</h2> -->
		<template #header="{ pageNum }">
			<p v-if="pageNum === 1">{{ pageNum }}</p>
			<p v-if="pageNum === 2">{{ pageNum }}</p>
			<p v-if="pageNum === 3">{{ pageNum }}</p>
			<p>header</p>
		</template>
		<template #main>
			<p>main</p>
		</template>
		<template #footer>
			<p>footer</p>
		</template>
		<h3>default</h3>
	</BaseCard>
	<BaseCard />
</template>

<style></style>
