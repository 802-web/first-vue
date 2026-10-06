<script setup>
import BaseIcon from '@/components/BaseIcon.vue'
import CountUp from '@/components/CountUp.vue'
import BaseButton from '@/components/BaseButton.vue'
</script>
<template>
	<p class="red">App</p>
	<CountUp id="baseBtn" class="border" />
	<BaseIcon />
	<BaseButton id="baseBtn" />
</template>

<style scoped>
.red {
	color: red;
}
</style>
