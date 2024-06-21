<!--COMPOSITION API-->
<!-- <script setup>
import { ref } from "vue";
const count = ref(0);

const addCount = () => {
  count.value = count.value + 1;
};

const subtractCount = () => {
  count.value = count.value - 1;
};
</script> -->

<!--OPTIONS API-->
<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    addToCount() {
      this.count = this.count + 1;
    },
    subtractFromCount() {
      this.count = this.count - 1;
    },
  },
};
</script>

<template>
  <main>
    <div>
      <h4>The current count is...</h4>
      <h1>{{ count }}</h1>
      <button @click="subtractCount()">-</button>
      <button @click="addCount()">+</button>
    </div>
  </main>
</template>

<style scoped>
main {
  background-color: aliceblue;
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;
}

div {
  text-align: center;
}
</style>
