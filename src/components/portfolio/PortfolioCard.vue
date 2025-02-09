<template>
  <article :class="$style['portfolio-card']">
    <img :class="$style['card-image']" :src="props.image" alt="Card image">
    <h4 :class="$style['card-title']">{{ props.title }}</h4>
    <div :class="$style['labels-wrapper']">
      <BaseLabel v-for="(label, index) in props.labels" :key="index" :text="label"></BaseLabel>
    </div>
    <BaseButton :text="props.buttonText" variant="secondary" :class="$style['card-button']"></BaseButton>
  </article>
</template>

<script setup>
import BaseLabel from '@/components/common/BaseLabel.vue';
import BaseButton from '@/components/common/BaseButton.vue';

const props = defineProps([
  "title",
  "labels",
  "buttonText",
  "image"
]);
</script>

<style lang="css" module>
.portfolio-card {
  border-radius: 10px;
  border: 1px solid #737373;
  padding: 20px;
}

.card-image {
  width: 100%;
  object-fit: cover;
  border-radius: 10px;
}

.card-title {
  font-size: 28px;
  font-weight: 700;
  margin: 20px 0 0 0;
}

.labels-wrapper {
  display: flex;
  gap: 8px;
  align-items: center;
  margin-top: 20px;
}

.card-button {
  width: 100%;
  margin-top: 20px;
}
</style>
