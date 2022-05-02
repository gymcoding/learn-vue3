<template>
	<div>
		<!-- @click="$emit('createPost', 1, 2, 3, '김길동')" -->
		<button class="btn btn-primary" @click="createPost">button</button>
	</div>
</template>

<script>
export default {
	setup(props, { emit }) {
		// context.emit
		const createPost = () => {
			emit('createPost', 111, 2, 3, '김길동');
		};
		return { createPost };
	},
};
</script>

<style lang="scss" scoped></style>
