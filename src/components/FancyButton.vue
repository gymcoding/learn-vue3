<template>
	<button class="fancy-btn">
		<slot><span>!!</span>Default Click!!</slot>
	</button>
</template>

<script>
export default {
	setup() {
		return {};
	},
};
</script>

<style scoped>
.fancy-btn {
	color: #fff;
	background: linear-gradient(315deg, #42d392 25%, #647eff);
	border: none;
	padding: 5px 12px;
	margin: 5px;
	border-radius: 8px;
	cursor: pointer;
}
</style>
