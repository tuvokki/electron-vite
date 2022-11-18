<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
const increaseCounter = () => {
  count.value = count.value + 2
}
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <button type="button" @click="increaseCounter">count is {{ count }}</button>
  </div>
  <p class="help-infos">Click the couter button to increase count.</p>
</template>

<style scoped>
.help-infos {
  color: #888;
}
</style>
