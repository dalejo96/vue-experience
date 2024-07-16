<script setup>
import GotCards from "./components/GoTCard.vue";
import RickAndMortyCards from "./components/RickAndMortyCard.vue";
import Hero from "./components/Hero.vue";
import { ref } from "vue";

const isGot = ref(true);
</script>

<template>
  <main>
    <Hero :isGot="isGot" @selectShow="isGot = !isGot" />

    <Suspense>
      <template #default>
        <KeepAlive>
          <Component :is="isGot ? GotCards : RickAndMortyCards" />
        </KeepAlive>
      </template>
      <template #fallback>
        <div class="cards spinner">
          <NSpin size="large" />
        </div>
      </template>
    </Suspense>
  </main>
</template>

<style scoped>
.cards {
  height: 700px;
  background-color: black;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
