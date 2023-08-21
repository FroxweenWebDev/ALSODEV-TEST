<template>
  <div class="consec">
		<p><strong>Input array: <i>{{ inputArray }}</i></strong></p>
    <p>Output array: <span>{{ uniqueSortedArray }}</span></p>
		
		
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputArray: [1, 3, 2, 2, 4, 3, 5, 6, 5],
    };
  },
  computed: {
    uniqueSortedArray() {
      const uniqueArray = [...new Set(this.inputArray)];
      const sortedArray = uniqueArray.sort((a, b) => a - b);
      return sortedArray;
    },
  },
};
</script>
