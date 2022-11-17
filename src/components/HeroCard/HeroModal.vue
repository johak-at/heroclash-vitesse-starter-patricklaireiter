<script setup>
const props = defineProps(['name', 'appearance', 'biography', 'connections', 'work'])
const emits = defineEmits(['hideBiography'])
</script>

<template>
  <div class="modal" @click="emits('hideBiography')">
    <ul>
      <li v-for="(value, key) in biography" :key="key">
        <p>{{ key }}: {{ value }}</p>
      </li><li v-for="(value, key) in appearance" :key="key">
        <p>{{ key }}: {{ value }}</p>
      </li><li v-for="(value, key) in work" :key="key">
        <p>{{ key }}: {{ value }}</p>
      </li><li v-for="(value, key) in connections" :key="key">
        <p>{{ key }}: {{ value }}</p>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.modal {
    position: fixed;
    text-align: left;
    padding: 5rem;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: orangered;
    }
</style>
