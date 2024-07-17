<script setup lang="ts">
import { ref } from "vue";

enum Gender {
  MALE,
  FEMALE,
}

const name = ref<string>("");
const gender = ref(Gender.MALE);
</script>

<template>
  <main>
    <div>
      <h1>People Invited to My Party</h1>
      <div class="input-container">
        <input type="text" placeholder="Name..." v-model="name" />
        <select v-model="gender">
          <option :value="Gender.MALE">Male</option>
          <option :value="Gender.FEMALE">Female</option>
        </select>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: antiquewhite;
}

input,
select {
  width: 100%;
  padding: 5px;
  margin-bottom: 2px;
}
</style>
