<template>
  <section :class="$style['stats-section']">
    <div :class="$style['stats-wrapper']">
      <p :class="$style['stats-text']"><span :class="$style['stats-text-big']">90%</span><br>Job Success<br>Score on Upwork</p>
      <img :src="dawn" alt="Stats star image">
      <p :class="$style['stats-text']"><span :class="$style['stats-text-big']">&gt;25.000</span><br>Duplicates on Figma<br>Community</p>
      <img :src="dawn" alt="Stats star image">
      <p :class="$style['stats-text']"><span :class="$style['stats-text-big']">&gt;2k</span><br>In Finished Works</p>
    </div>
  </section>
</template>

<script setup>
import dawn from '@/assets/images/dawn.svg';
</script>

<style lang="css" module>
.stats-section{
  width: 100%;
  padding: 70px 22px 100px 22px;
}

.stats-wrapper {
  border-radius: 30px;
  background-color: #0B0B0B;
  border: 1px solid #646464;
  padding: 80px 0;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 70px;
  text-align: center;
}

.stats-text {
  color: var(--color-green);
  font-size: 22px;
  font-weight: 300;
  font-family: var(--font-family-secondary);
  letter-spacing: 1px;
}

.stats-text-big {
  font-size: 64px;
  font-weight: 700;
  letter-spacing: 3px;
}

.stats-section img {
  display: none;
  width: 80px;
  height: 80px;
}

@media screen and (min-width: 640px) {
  .stats-section {
    padding: 70px 22px 100px 22px;
  }
}

@media screen and (min-width: 1024px) {
  .stats-section {
    padding: 70px 80px 150px 80px;
  }

  .stats-wrapper {
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 3%;
  }

  .stats-section img {
    display: block;
  }
}

@media screen and (min-width: 1536px) {
  .stats-section {
    padding: 70px 80px 200px 80px;
  }
}
</style>
