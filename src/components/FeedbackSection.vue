<template>
  <section :class="$style['feedback-section']">
    <cite :class="$style['user-name']">Kaleb Lechtenberg</cite>
    <blockquote :class="$style['user-feedback']">"Working with this freelancer has been great. His attention to detail is unparalleled and finished all work ahead of schedule. Will gladly send more work and I do not hesitate to recommend him to you on your project also."</blockquote>
    <img :class="$style['shield-image']" :src="shield" alt="Shield image"/>
  </section>
</template>

<script setup>
import shield from '@/assets/images/shield.svg';
</script>

<style lang="css" module>
.feedback-section {
  padding: 60px 0;
  gap: 20px;
  background: url('../assets/images/gradient-bg.png');
  background-size: cover;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.user-name {
  font-weight: 700;
  font-style: normal;
  width: 90%;
  font-size: 20px;
}

.user-feedback {
  font-weight: 700;
  font-style: italic;
  width: 90%;
  font-size: 20px;
}

.shield-image {
  height: auto;
  width: 36px;
}

@media screen and (min-width: 640px) {
  .feedback-section {
    padding: 100px 0;
    gap: 30px;
  }

  .user-name {
    width: 85%;
    font-size: 28px;
  }

  .user-feedback {
    width: 85%;
    font-size: 28px;
  }

  .shield-image {
    width: 54px;
  }
}

@media screen and (min-width: 1024px) {
  .feedback-section {
    padding: 147px 0;
    gap: 60px;
  }

  .user-name {
    width: 80%;
    font-size: 40px;
  }

  .user-feedback {
    width: 80%;
    font-size: 40px;
  }

  .shield-image {
    width: 68px;
  }
}

@media screen and (min-width: 1536px) {
  .user-name {
    width: 70%;
    font-size: 48px;
  }

  .user-feedback {
    width: 70%;
    font-size: 48px;
  }

  .shield-image {
    width: 72px;
  }
}
</style>
