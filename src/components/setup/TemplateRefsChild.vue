<template>
	<div>
		{{ $parent }}
		<ul>
			<li v-for="fruit in $parent.fruits" :key="fruit">{{ fruit }}</li>
		</ul>
	</div>
</template>

<script setup>
import { ref } from 'vue';

const message = ref('Hello ~!');
const sayHello = () => {
	alert(message.value);
};
defineExpose({
	message,
	sayHello,
});
</script>

<style lang="scss" scoped></style>
