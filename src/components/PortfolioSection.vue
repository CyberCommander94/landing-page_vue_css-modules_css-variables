<template>
  <section id="portfolio" :class="$style['portfolio-section']">
    <h3 :class="$style['portfolio-title']">PORTFOLIO</h3>
    <div :class="$style['portfolio-wrapper']">
      <PortfolioCard v-for="(elem, index) in cardsData" :key="index" :title="elem.title" :labels="elem.labels" :buttonText="elem.buttonText" :image="elem.image"></PortfolioCard>
    </div>
  </section>
</template>

<script setup>
import { readonly } from 'vue';
import PortfolioCard from '@/components/portfolio/PortfolioCard.vue';
import photo1 from '@/assets/images/preview.png';

const cardsData = readonly([
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
  {
    title: "Mi portal U",
    labels: ["UX Design", "University", "JavaScript"],
    buttonText: "Figma community",
    image: photo1
  },
]);
</script>

<style lang="css" module>
.portfolio-section {
  width: 100%;
  padding: 70px 22px 100px 22px;
}

.portfolio-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-auto-rows: auto;
  row-gap: 40px;
  column-gap: 20px;
}

.portfolio-title {
  font-family: var(--font-family-secondary);
  font-weight: 100;
  margin: 0;
  font-size: 64px;
  margin-bottom: 50px;
}

@media screen and (min-width: 640px) {
  .portfolio-section {
    padding: 70px 22px 100px 22px;
  }

  .portfolio-wrapper {
    grid-template-columns: 1fr 1fr;
  }

  .portfolio-title {
    font-size: 44px;
  }
}

@media screen and (min-width: 1024px) {
  .portfolio-section {
    padding: 70px 80px 150px 80px;
  }

  .portfolio-title {
    font-size: 64px;
  }
}

@media screen and (min-width: 1536px) {
  .portfolio-wrapper {
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: 1fr 1fr;
  }

  .portfolio-wrapper {
    grid-template-columns: 1fr 1fr 1fr 1fr;
  }

  .portfolio-section {
    padding: 70px 80px 200px 80px;
  }
}
</style>
