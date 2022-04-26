<template>
	<div>
		<button @click="printEventInfo('Hello Vue3', $event)">
			inline event handler
		</button>
		<hr />
		<input type="text" @keyup="onKeyupHandler" />
	</div>
</template>

<script>
export default {
	setup() {
		const printEventInfo = (message, event) => {
			console.log('message: ', message);
			console.log('event.target: ', event.target);
			console.log('event.target.tagName: ', event.target.tagName);
		};
		const onKeyupHandler = event => {
			console.log('event.key: ', event.key);
		};
		return { printEventInfo, onKeyupHandler };
	},
};
</script>

<style lang="scss" scoped></style>
