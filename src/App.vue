<template>
  <div>
    <header>
      <TheNavigation :destinations="destinations"></TheNavigation>
    </header>
    <div class="container">
      <router-view :destinations="destinations"></router-view>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import TheNavigation from './components/TheNavigation.vue';

const destinations = ref([]);
</script>
