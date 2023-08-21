<template>
	<div class="consec">
		<p>Input array: <strong><i>{{ array }}</i></strong></p>
		<p>Consecutive: <span :class="spanClass">{{ isConsecutive ? 'true' : 'false' }}</span></p>
	</div>
</template>

<script>
export default {
	props: {
		array: {
			type: Array,
			required: true
		}
	},
	computed: {
		isConsecutive() {
			const sortedArray = [...this.array].sort((a, b) => a - b);
			for (let i = 1; i < sortedArray.length; i++) {
				if (sortedArray[i] - sortedArray[i - 1] !== 1) {
					return false;
				}
			}
			return true;
		},
		spanClass() {
      return this.isConsecutive ? 'true' : 'false';
    }
	}
};
</script>
