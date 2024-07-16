<script setup>
import axios from "axios";
import { ref } from "vue";
import Card from "./Card.vue";

const characters = ref(null);
const response = await axios.get("https://thronesapi.com/api/v2/Characters");
characters.value = response.data;
</script>

<template>
  <div class="container">
    <div class="cards">
      <Card
        v-for="character in characters"
        :key="character.id"
        :image="character.imageUrl"
        :name="character.fullName"
      >
        <p>{{ character.title }}</p>
      </Card>
    </div>
  </div>
</template>

<style scoped>
.container {
  background-color: rgb(27, 26, 26);
  padding: 30px;
}
.cards {
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
}
.cards h3 {
  font-weight: bold;
}
.cards p {
  font-size: 10px;
}

.button-container {
  display: flex;
  justify-content: center;
  padding-top: 30px;
}
.button-container button {
  border: none;
  width: 50px;
  height: 50px;
  border-radius: 100%;
  margin: 0 5px;
  cursor: pointer;
}
</style>
