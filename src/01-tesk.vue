<template>
  <div>
    <ul>
      <li v-for="(item, index) in arr" :key="index">{{ item }}</li>
    </ul>
    <button @click="reverseFn">走一走</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: ["美女", "程序猿", "帅哥"],
    };
  },
  methods: {
    reverseFn(){
      this.arr.push(this.arr[0])
      this.arr.shift()
    }
  },
};
</script>

<style></style>
