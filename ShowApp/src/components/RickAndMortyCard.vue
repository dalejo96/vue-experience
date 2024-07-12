<script setup>
import axios from "axios";
import { ref, watch } from "vue";
const characters = ref(null);
const page = ref(1);

const response = await axios.get("https://rickandmortyapi.com/api/character/?page=1");
characters.value = response.data;

watch(page, async () => {
  const response = await axios.get(`https://rickandmortyapi.com/api/character/?page=${page.value}`);
  characters.value = response.data;
});
</script>

<template>
  <div>
    <h1>Rick and Morty Cards</h1>
    <p>{{ characters }}</p>
    <div>
      <button @click="page = page + 1">Next</button>
      <button @click="page = page - 1">Back</button>
    </div>
  </div>
</template>
