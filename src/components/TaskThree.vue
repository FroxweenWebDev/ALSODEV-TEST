<template>
  <div class="consec">
		<p>Input array: <strong><i>{{ arrayOf }}</i></strong></p>
    <p>Output array: <span>{{ arrayOfOutput }}</span></p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arrayOf: [1, 3, 2, 2, 4, 3, 5, 6, 5, 17, 200, 200, 26, 35, 15, 55. ], 
			arrayIn: [1, 3, 2, 2, 4, 3, 5, 6, 5, 17, 200, 200, 26, 35, 15, 55. ],
      arrayOfOutput: [],
    };
  },
  methods: {
    getCountArray(arrayOf) {
      const countMap = new Map();

      arrayOf.forEach(number => {
        if (countMap.has(number)) {
          countMap.set(number, countMap.get(number) + 1);
        } else {
          countMap.set(number, 1);
        }
      });

      const arrayOfOutput = [];
      countMap.forEach((count, number) => {
        const obj = {};
        obj[number] = count;
        arrayOfOutput.push(obj);
      });

      return arrayOfOutput;
    },
  },
  created() {
    this.arrayOfOutput = this.getCountArray(this.arrayOf);
  },
};
</script>
