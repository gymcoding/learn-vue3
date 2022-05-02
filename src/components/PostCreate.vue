<template>
	<div>
		<!-- @click="$emit('createPost', 1, 2, 3, '김길동')" -->
		<input v-model="title" type="text" class="form-control" />

		<button class="btn btn-primary" @click="createPost">button</button>
	</div>
</template>

<script>
import { ref } from 'vue';

export default {
	// emits: ['createPost'],
	emits: {
		createPost: newTitle => {
			console.log('validator: ', newTitle);
			if (!newTitle) {
				return false;
			}
			return true;
		},
	},
	setup(props, { emit }) {
		// context.emit
		const title = ref('');
		const createPost = () => {
			emit('createPost', title.value);
		};
		return { createPost, title };
	},
};
</script>

<style lang="scss" scoped></style>
