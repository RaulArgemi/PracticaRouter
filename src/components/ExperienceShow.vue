<template>
  <section>
    <h1>{{experience.name}}</h1>
    <img :src="`/images/${experience.image}`" :alt="experience.name" class="large-image">
    <p>{{experience.description}}</p>
  </section>
</template>
<script>
import sourceData from '@/data.json';

export default {
  props:{
    id: {type: Number, required: true,},
    experienceSlug: {type: String, required: true,}
  },
  computed:{
    destination(){
      return sourceData.destinations.find(
        destination => destination.id === this.id
      )
    },
    experience(){
      return this.destination.experiences.find(
        experience=> experience.slug === this.experienceSlug
      )
    }
  }
}
</script>

<style scoped>
.large-image {
  width: 500px;
  max-width: 800px;
  height: auto;
}
</style>