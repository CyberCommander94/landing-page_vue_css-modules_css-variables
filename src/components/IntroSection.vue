<template>
  <section :class="$style['intro-section']">
    <div :class="$style['intro-text-wrapper']">
      <p :class="$style['intro-text']">
        <span :class="$style['intro-text-top']">PRODUCT<br>DESIGNER</span><br>
        <span :class="$style['intro-text-bottom']">CRISTIAN MUÑOZ</span>
      </p>
      <div :class="$style['intro-social-wrapper']">
        <button>
          <img :src="instagram" alt="Instagram image">
        </button>
        <button>
          <img :src="figma" alt="Figma image">
        </button>
        <button>
          <img :src="linkedin" alt="LinkedIn image">
        </button>
        <button>
          <img :src="twitter" alt="Twitter image">
        </button>
        <button>
          <img :src="telegram" alt="Telegram image">
        </button>
        <button>
          <img :src="medium" alt="Medium image">
        </button>
      </div>
      <BaseButton :class="$style['intro-button']" variant="secondary" text="Download Curriculum Vitae" :icon="arrow"></BaseButton>
    </div>
    <div>
      <img :class="$style['star-image']" :src="star" alt="Star image">
    </div>
    <div>
      <img :class="$style['intro-image']" :src="introImage" alt="Intro image">
    </div>
  </section>
</template>

<script setup>
import star from '@/assets/images/star.svg';
import arrow from '@/assets/images/arrow-down.svg';
import instagram from '@/assets/images/instagram.png';
import figma from '@/assets/images/figma.png';
import linkedin from '@/assets/images/linkedin.png';
import twitter from '@/assets/images/twitter.png';
import telegram from '@/assets/images/telegram.png';
import medium from '@/assets/images/medium.png';
import introImage from '@/assets/images/intro-image.png';
import BaseButton from '@/components/common/BaseButton.vue';
</script>

<style lang="css" module>
.intro-section {
  width: 100%;
  padding: 140px 22px 50px 22px;
  display: flex;
  justify-content: center;
  box-sizing: border-box;
}

.intro-image,
.star-image {
  display: none;
}

.intro-button {
  width: 100%;
  margin-top: 30px;
}

.intro-social-wrapper {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 5px;
  margin-top: 50px;
}

.intro-social-wrapper > button {
  width: 40px;
  height: 40px;
  background-color: transparent;
  border: 1px solid var(--color-white);
  border-radius: 10px;
  cursor: pointer;
}

.intro-social-wrapper > button > img {
  width: 100%;
  object-fit: cover;
}

.intro-text-wrapper {
  width: 100%;
}

.intro-text {
  color: var(--color-white);
  font-family: var(--font-family-secondary);
  margin: 0;
  text-align: center;
}

.intro-text-top {
  font-size: 70px;
  line-height: 80px;
  display: inline-block;
}

.intro-text-bottom {
  font-size: 40px;
  background-image: linear-gradient(to right, #FA709A, #FEE140);
  color: transparent;
  background-clip: text;
  margin-top: 10px;
  display: block;
  line-height: 58px;
  display: inline-block;
}

@media screen and (min-width: 640px) {
  .intro-section {
    padding: 170px 22px 50px 22px;
  }

  .intro-social-wrapper > button {
    width: 52px;
    height: 52px;
  }

  .intro-text-wrapper {
    width: 70%;
  }

  .intro-text-top {
    font-size: 112px;
    line-height: 112px;
  }

  .intro-text-bottom {
    font-size: 60px;
    line-height: 82px;
  }
}

@media screen and (min-width: 1024px) {
  .intro-section {
    padding: 170px 80px 75px 80px;
    grid-template-columns: 45% 10% 45%;
  }

  .intro-image,
  .star-image {
    width: 100%;
    object-fit: cover;
    display: block;
  }

  .intro-button {
    width: 100%;
    margin-top: 30px;
  }

  .intro-social-wrapper {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 5px;
    margin-top: 50px;
  }

  .intro-social-wrapper > button {
    width: 52px;
    height: 52px;
  }

  .intro-text-wrapper {
    width: 100%;
  }

  .intro-text {
    text-align: left;
  }

  .intro-text-top {
    font-size: 112px;
    line-height: 112px;
  }

  .intro-text-bottom {
    font-size: 60px;
    line-height: 82px;
  }
}

@media screen and (min-width: 1536px) {
  .intro-section {
    padding: 170px 80px 100px 80px;
  }
}
</style>
