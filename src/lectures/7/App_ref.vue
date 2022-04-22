<template>
	<div>
		<h2>State Message</h2>
		<p>{{ state.message }}</p>
		<button v-on:click="addStateMessage">click</button>
		<!-- <h2>Message</h2>
		<p>{{ message.value }}</p>
		<button v-on:click="addMessage">click</button> -->
		<h2>Ref: Messsage</h2>
		<p>{{ message }}</p>
		<button v-on:click="addMessage">click</button>
	</div>
</template>

<script>
import { reactive, ref } from 'vue';

export default {
	setup() {
		const state = reactive({
			message: 'Hello Vue3',
		});
		const addStateMessage = () => {
			state.message = state.message + '!';
		};

		// let message = reactive({
		// 	value: 'Hello Vue3',
		// });
		// const addMessage = () => {
		// 	message.value = message.value + '!';
		// };

		const message = ref('Hello Ref!');
		const addMessage = () => {
			message.value = message.value + '!';
		};
		return {
			state,
			addStateMessage,
			message,
			addMessage,
		};
	},
};
</script>

<style lang="scss" scoped></style>
