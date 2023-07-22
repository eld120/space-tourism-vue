<script setup lang="ts">
import json from '../assets/data.json';
import NavBar from './components/NavBar.vue';

</script>

<template>
  <NavBar /> 
  <main>
    So, you want to travel to
    {{ json.destinations[1].name}}
    Let’s face it; if you want to go to space, you might as well genuinely go to
    outer space and not hover kind of on the edge of it. Well sit back, and relax
    because we’ll give you a truly out of this world experience!
    Explore
  </main>
</template>

<style scoped lang="sass">
  main
    min-height: 100%
  
</style>
