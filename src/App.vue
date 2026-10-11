<script setup>
import ShowCount from '@/components/ShowCount.vue'
import ResetButton from '@/components/ResetButton.vue'
import BaseCard from '@/components/BaseCard.vue'
import ComponentA from '@/components/ComponentA.vue'
import ComponentB from '@/components/ComponentB.vue'
import ComponentC from '@/components/ComponentC.vue'
import { ref, shallowRef } from 'vue'

const count = ref(0)
const onReset = (val) => {
	count.value = val
	return count.value
}

const currentComp = shallowRef(ComponentA)
</script>
<template>
	<!-- <ShowCount bar="bar" /> -->
	<!-- <ShowCount :foo="count" />
	<button @click="count++">+1</button>
	<ResetButton @reset="count = $event" />
	<ResetButton @reset-count="onReset" /> -->

	<h1>Dynamic Component</h1>
	<button @click="currentComp = ComponentA">A</button>
	<button @click="currentComp = ComponentB">B</button>
	<button @click="currentComp = ComponentC">C</button>
	<!-- <KeepAlive include="ComponentC,ComponentB" exclude="ComponentA"> -->
	<KeepAlive>
		<component :is="currentComp" />
	</KeepAlive>

	<h1>Slots</h1>
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
