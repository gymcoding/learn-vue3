<template>
	<div class="card">
		<div class="card-header">
			<slot name="header">#Header</slot>
		</div>
		<div class="card-body">
			<slot>#Body</slot>
		</div>
		<div class="card-footer text-muted">
			<slot name="footer">#Footer</slot>
		</div>
	</div>
</template>

<script>
export default {
	setup() {
		return {};
	},
};
</script>

<style lang="scss" scoped></style>
