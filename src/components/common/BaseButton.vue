<template>
  <button
    :class="[props.variant === 'primary' ? $style.primary : $style.secondary, $style.btn]"
  >
    <div :class="$style['button-content-wrapper']">
      <slot>
        <span :class="$style['button-text']">{{ props.text }}</span>
        <img v-if="props.icon" :src="props.icon" alt="Icon" :class="$style['button-image']" />
      </slot>
    </div>
  </button>
</template>

<script lang="ts" setup>
import { defineProps, withDefaults } from 'vue'

interface Props {
  icon?: string
  text?: string
  variant?: 'primary' | 'secondary'
}

const props = withDefaults(defineProps<Props>(), {
  variant: 'primary',
  text: 'button',
})

</script>

<style lang="css" module>

.btn {
  border: none;
  outline: none;
  font-weight: 300;
  font-size: 16px;
  transition: background 0.4s ease;
  padding: 12px 24px;
  display: block;
  cursor: pointer;
}

.button-content-wrapper {
  display: flex;
  gap: 8px;
  align-items: center;
  justify-content: center;
}

.button-text,
.button-image {
  display: block;
}

.primary {
  background-color: var(--color-purple-dark);
  color: var(--color-white);
  border-radius: 4px;
}

.secondary {
  background-color: var(--color-gray);
  color: var(--color-white);
}

.primary:hover {
  background-color: var(--color-purple-medium);
}

.secondary:hover {
  color: #ffffff;
  background-color: #3E3C3C;
}
</style>
