<template>
  <article :class="$style['skills-card']">
    <div :class="$style['percent-wrapper']">
      <span :class="$style['percent']">97%</span>
    </div>
    <div :class="$style['skill-text-wrapper']">
      <h4 :class="$style['skill-title']">{{ props.title }}</h4>
      <p :class="$style['skill-text']">{{ props.text }}</p>
    </div>
  </article>
</template>

<script setup>
const props = defineProps([
  "title",
  "text"
]);
</script>

<style lang="css" module>
.skills-card {
  padding: 40px;
  border-radius: 10px;
  border: 1px solid #737373;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}

.percent-wrapper {
  width: 220px;
  height: 220px;
  min-width: 220px;
  min-height: 220px;
  background: url('../../assets/images/graph.png') no-repeat;
  background-size: cover;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 36px;
}

.skill-text-wrapper {
  text-align: center;
}

.skill-title {
  font-weight: 700;
  font-size: 36px;
  margin: 20px 0;
}

.skill-text {
  font-weight: 300;
  font-size: 20px;
}

@media screen and (min-width: 1024px) {
  .skills-card {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }

  .skill-text-wrapper {
    text-align: left;
  }
}
</style>
