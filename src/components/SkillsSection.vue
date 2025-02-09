<template>
  <section id="skills" :class="$style['skills-section']">
    <h3 :class="$style['skills-title']">SKILLS</h3>
    <div :class="$style['skills-wrapper']">
      <SkillsCard v-for="(elem, index) in cardsData" :key="index" :title="elem.title" :text="elem.text"></SkillsCard>
    </div>
  </section>
</template>

<script setup>
import { readonly } from 'vue';
import SkillsCard from '@/components/skills/SkillsCard.vue';

const cardsData = readonly([
  {
    title: "UX Design",
    text: "UI design is the process of designing the visual and interactive elements of a user interface, such as buttons, icons, and layout, to create an intuitive and pleasing experience for users.",
  },
  {
    title: "UI Design",
    text: "UI design is the process of designing the visual and interactive elements of a user interface, such as buttons, icons, and layout, to create an intuitive and pleasing experience for users.",
  },
  {
    title: "Information Architecture",
    text: "Information architecture is the design of the structure and organization of content on a website or digital product to make it easy for users to navigate and understand.",
  },
  {
    title: "Figma",
    text: "Figma is a cloud-based design tool that allows teams to collaborate on the design process in real time. It offers a range of features for designing, prototyping, and sharing user interfaces.",
  },
]);
</script>

<style lang="css" module>
.skills-section {
  width: 100%;
  padding: 70px 22px 100px 22px;
}

.skills-wrapper {
  display: grid;
  grid-template-columns: 1fr;
  grid-auto-rows: auto;
  gap: 20px;
}

.skills-title {
  font-family: var(--font-family-secondary);
  font-weight: 100;
  margin: 0;
  font-size: 64px;
  margin-bottom: 50px;
}

@media screen and (min-width: 640px) {

  .skills-section {
    padding: 70px 22px 100px 22px;
  }

  .skills-title {
    font-size: 44px;
  }
}

@media screen and (min-width: 1024px) {
  .skills-section {
    padding: 70px 80px 150px 80px;
  }

  .skills-title {
    font-size: 64px;
  }
}

@media screen and (min-width: 1536px) {
  .skills-wrapper {
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: 1fr 1fr;
  }

  .skills-section {
    padding: 70px 80px 200px 80px;
  }
}
</style>
