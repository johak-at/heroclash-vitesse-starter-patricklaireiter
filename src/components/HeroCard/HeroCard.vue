<script setup>
const props = defineProps(['hero'])
const showBiography = ref(false)
</script>

<template>

  <div grid class="heroCard">
    <HeroImage :image-url="hero.images.md" @showBiography="showBiography = true" />
    <HeroStats :name="hero.name" :stats="hero.powerstats" :alignment="hero.biography.alignment" />
    <HeroModal  v-if="showBiography" :name="hero.name" :appearance="hero.appearance" :biography="hero.biography" :connections="hero.connections" :work="hero.work" @hideBiography="showBiography = false"
  />
  </div>
</template>

<style scoped>
.heroCard {
    grid-template-columns: 1fr 1.2fr;
}
</style>
