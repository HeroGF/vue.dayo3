<template>
  <div>
    <ul>
      <li v-for="(item, index) in myArr" :key="index">
        {{ item }}
        <button @click="delFn(index)">删除</button>
      </li>
    </ul>
    <button @click="addFn">生成</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      myArr: [1, 5, 3],
    };
  },
  methods: {
    addFn() {
      this.myArr.push(Math.floor(Math.random() * 20) + 1);
    },
    delFn(index) {
      this.myArr.splice(index, 1);
    },
  },
};
</script>

<style></style>
