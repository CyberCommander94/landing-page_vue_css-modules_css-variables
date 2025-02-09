<template>
  <header :class="$style.header">
    <img width="73" height="27" :src="logo" alt="Logo" :class="$style.logo">

    <button :class="$style.burger" @click="isOpen = !isOpen" aria-label="Toggle menu">
      <img v-if="!isOpen" width="40" height="40" :src="menu" alt="Menu icon" :class="$style.menu">
      <img v-else width="26" height="26" style="padding: 7px 7px; box-sizing: content-box;" :src="close" alt="Close menu icon" :class="$style.menu">
    </button>
    <nav :class="[$style.nav, { [$style.open]: isOpen, [$style.closed]: !isOpen }]" aria-label="Main menu">
      <ul :class="[$style['nav-list']]">
        <li><a href="#">Home</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#about">About Me</a></li>
        <li :class="$style['contact-btn-xs']"><BaseButton text="Contact Me"></BaseButton></li>
      </ul>
    </nav>

    <BaseButton :class="$style['contact-btn-sm']" text="Contact Me"></BaseButton>
  </header>
</template>

<script setup>
import { ref } from 'vue';
import BaseButton from '@/components/common/BaseButton.vue';
import logo from '@/assets/images/logo.png';
import menu from '@/assets/images/menu.png';
import close from '@/assets/images/close.png';

const isOpen = ref(false);
</script>

<style lang="css" module>
header {
  width: 100%;
  padding: 16px 22px 16px 22px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: var(--color-dark);
  position: fixed;
  top: 0;
  left: 0;
}

.closed {
  display: none !important;
}

.open {
  display: flex;
}

.logo {
  position: relative;
  z-index: 2;
}

.nav {
  position: absolute;
  right: 0;
  top: 0;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: flex-end;
  background-color: var(--color-dark);
}

.nav-list {
  display: flex;
  flex-direction: column;
  list-style-type: none;
  height: 100%;
  background-color: var(--color-gray);
  padding: 100px 16px 10px 16px;
  margin: 0;
  box-sizing: border-box;
}

.nav-list li {
  justify-self: flex-end;
  margin-bottom: 10px;
}

.nav-list li:last-child {
  position: relative;
  bottom: 0;
  height: 100%;
  display: flex;
  align-items: flex-end;
}

.nav-list a {
  display: block;
  text-decoration: none;
  font-size: 18px;
  color: var(--color-white);
  font-weight: 300;
  padding: 8px 16px;
  border-radius: 4px;
}

.nav-list a:hover {
  background-color: var(--color-purple-dark);
}

.contact-btn-xs {
  display: block;
  margin-top: 15px;
  width: 100%;
}

.contact-btn-sm {
  display: none;
}

.burger {
  display: block;
  background-color: transparent;
  border: none;
  outline: none;
  border-radius: 4px;
  z-index: 1;
  cursor: pointer;
  padding: 0;
}

@media screen and (min-width: 640px) {
  header {
    padding-top: 30px;
    padding-bottom: 30px;
    justify-content: space-between;
    gap: 10px;
  }

  .nav {
    position: relative;
    display: flex !important;
    height: auto;
    width: auto;
  }

  .nav-list {
    list-style-type: none;
    flex-direction: row;
    background-color: transparent;
    height: auto;
    flex-direction: row;
    padding: 0;
    align-items: center;
    gap: 3px;
  }

  .nav-list a{
    text-decoration: none;
    font-size: 18px;
    color: var(--color-white);
    font-weight: 300;
    padding: 11px 16px;
  }

  .contact-btn-xs {
    display: none !important;
  }

  .contact-btn-sm {
    display: block;
  }

  .burger {
    display: none;
  }

  .nav-list li {
    margin: 0;
  }
}

@media screen and (min-width: 1024px) {
  header {
    padding: 30px 60px;
  }
}

@media screen and (min-width: 1536px) {
  header {
    padding: 30px 80px;
  }
}
</style>
