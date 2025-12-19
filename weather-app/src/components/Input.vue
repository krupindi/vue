<script setup>
import { onMounted, onUnmounted, onUpdated } from "vue";

const data = defineModel({ type: String, required: true });

onMounted(() => {
  console.log("Input mounted");
});

onUpdated(() => {
  console.log("Input updated");
});

onUnmounted(() => {
  console.log("input unmounted");
});
</script>

<template>
  <input v-model="data" class="input" />
</template>

<style scoped>
.input {
  color: var(--color-primary);
  border-radius: 10px;
  height: 53px;
  border: none;
  padding: 15px 20px;
  font-size: 18px;
  box-shadow: 1px 2px 4px 0 var(--color-bg-main);
  background: var(--color-bg-card);
}

.input::placeholder {
  color: var(--color-text-placeholder);
}
</style>
