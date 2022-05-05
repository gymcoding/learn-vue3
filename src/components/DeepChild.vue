<template>
	<div class="card">
		<div class="card-header">Deep Child Component</div>
		<div class="card-body">
			<p>staticMessage: {{ staticMessage }}</p>
			<p>message: {{ message }}</p>
			<p>count: {{ count }}</p>
		</div>
	</div>
</template>

<script>
import { inject } from 'vue';

export default {
	setup() {
		const staticMessage = inject('static-message', 'default message');
		const { message, updateMessage } = inject('message');
		updateMessage('!');
		message.value = message.value + '!';
		const count = inject('count');
		return { staticMessage, message, count };
	},
};
</script>

<style lang="scss" scoped></style>
