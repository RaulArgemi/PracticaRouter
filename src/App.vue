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

<script>
import TheNavigation from "./components/TheNavigation.vue";

export default {
  components: {
    TheNavigation,
  },
  data() {
    return {
      destinations: [],
    };
  },
};
</script>

<style>
/* Estilos aquí */
</style>
