<template>
	<div class="container py-4">
		<input ref="inputRef" type="text" value="hello world!" />
		<!-- <LifecycleChild></LifecycleChild> -->
		<p id="message">{{ message }}</p>
	</div>
</template>

<script>
import { onBeforeMount, onBeforeUpdate, onMounted, onUpdated, ref } from 'vue';
// import LifecycleChild from './LifecycleChild.vue';
export default {
	components: {
		// LifecycleChild,
	},
	setup() {
		// console.log('setup');
		const inputRef = ref(null);
		const message = ref('');
		// onBeforeMount(() => {
		// 	console.log('onBeforeMount', inputRef.value);
		// });
		// onMounted(() => {
		// 	console.log('onMounted', inputRef.value.value);
		// });

		onBeforeUpdate(() => {
			console.log('onBeforeUpdate', message.value);
			console.log(
				'DOM Content: ',
				document.querySelector('#message').textContent,
			);
		});
		onUpdated(() => {
			console.log('onUpdated', message.value);
			console.log(
				'DOM Content: ',
				document.querySelector('#message').textContent,
			);
		});
		return { inputRef, message };
	},
	// data: () => ({
	// 	dataMessage: 'data message',
	// }),
	// beforeCreate() {
	// 	console.log('beforeCreate', this.dataMessage);
	// },
	// created() {
	// 	console.log('created', this.dataMessage);
	// 	console.log(this);
	// },
};
</script>

<style lang="scss" scoped></style>
