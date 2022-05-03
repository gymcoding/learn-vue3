<template>
	<label>
		{{ label }}
		<!-- v-model="username" -->
		<input v-model="value" type="text" />
		<!-- :value="modelValue"
			@input="event => $emit('update:modelValue', event.target.value)" -->
	</label>
</template>

<script>
import { computed } from '@vue/reactivity';

export default {
	props: ['modelValue', 'label'],
	emits: ['update:modelValue'],
	setup(props, { emit }) {
		const value = computed({
			get() {
				return props.modelValue;
			},
			set(value) {
				emit('update:modelValue', value);
			},
		});
		return { value };
	},
};
</script>

<style lang="scss" scoped></style>
