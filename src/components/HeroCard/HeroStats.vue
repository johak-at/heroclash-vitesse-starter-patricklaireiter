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
  background-color: red;
 }

 .good{
  background-color: yellow;
 }
</style>
