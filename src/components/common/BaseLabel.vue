<template>
  <span :class="$style['base-label']">{{ props.text }}</span>
</template>

<script setup>
const props = defineProps([
  "text",
]);
</script>

<style lang="css" module>
.base-label {
  padding: 3px 8px;
  border-radius: 12px;
  font-weight: 300;
  font-size: 12px;
  color: #784DC7;
  background-color: var(--color-purple-light);
  border: 1px solid var(--color-purple-medium);
  cursor: pointer;
}

.base-label:hover {
  background-color: #dac9f9;
}
</style>
