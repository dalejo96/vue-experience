<script setup>
import GotCards from "./components/GoTCard.vue";
import RickAndMortyMCards from "./components/RickAndMortyCard.vue";
</script>

<template>
  <main>
    <h1>Hero</h1>
    <Suspense>
      <template #default>
        <RickAndMortyMCards />
      </template>
      <template #fallback>
        <div><p>Loading...</p></div>
      </template>
    </Suspense>
  </main>
</template>
