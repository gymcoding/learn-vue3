<template>
	<div>
		<p>
			{{ counter }}
		</p>
		<p>
			{{ message }}
		</p>
		<button @click="increment">click!</button>
	</div>
</template>

<script>
import { ref } from 'vue';

export default {
	setup() {
		const counter = ref(0);
		const message = ref('Hello Vue3');
		const increment = () => {
			counter.value++;
		};
		return {
			counter,
			message,
			increment,
		};
	},
};
</script>

<style lang="scss" scoped></style>
