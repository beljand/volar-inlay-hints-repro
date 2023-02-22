<template>
	<div>test</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
	name: "TestComponent",
	components: {},
	props: {
		size: {
			type: String,
			default: "md",
			validator: function (value: string) {
				return ["md", "sm"].indexOf(value) > -1;
			},
		},
	},
	data() {
		return {
			test: 'test'
		};
	},
});
</script>
