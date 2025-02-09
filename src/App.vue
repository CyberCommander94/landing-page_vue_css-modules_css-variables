<template>
  <div :class="$style['main-content-wrapper']">
    <HeaderSection></HeaderSection>
    <IntroSection></IntroSection>
    <StatsSection></StatsSection>
    <PortfolioSection></PortfolioSection>
    <SkillsSection></SkillsSection>
    <FeedbackSection></FeedbackSection>
    <AboutSection></AboutSection>
    <FooterSection></FooterSection>
  </div>
</template>

<script setup>
import HeaderSection from './components/HeaderSection.vue';
import IntroSection from './components/IntroSection.vue';
import StatsSection from './components/StatsSection.vue';
import PortfolioSection from './components/PortfolioSection.vue';
import SkillsSection from './components/SkillsSection.vue';
import FeedbackSection from './components/FeedbackSection.vue';
import AboutSection from './components/AboutSection.vue';
import FooterSection from './components/FooterSection.vue';

</script>

<style lang="css" module>
  .main-content-wrapper {
    width: 100vw;
    height: 100vh;
    box-sizing: border-box;
  }
</style>
