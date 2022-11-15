<script setup>
const props = defineProps(['name', 'stats', 'alignment'])
</script>

<template>
  <div :class="alignment">
    <h1>{{ name }}</h1>
    <StatField v-for="(value, key) in stats" :key="key" :skill="key" :value="value" />
  </div>
</template>

<style scoped>
 *{border: 1px solid red}

 .bad{
  background-image: linear-gradient(135deg, #f12711, #f5af19);
 }

 .good{
  background-image: linear-gradient(135deg, teal, pink);
 }

 .neutral{
  background-image: linear-gradient(135deg, #f12711, #f5af19);
 }
</style>
