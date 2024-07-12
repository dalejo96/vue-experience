<script setup>
    import axios from 'axios'
import { ref } from 'vue';
    const characters = ref(null)
    const response = await axios.get('https://thronesapi.com/api/v2/Characters')
    characters.value = response.data
    
</script>

<template>
  <div>
    <h1>Game of Thrones Cards</h1>
    <h1>{{ characters }}</h1>
  </div>
</template>
