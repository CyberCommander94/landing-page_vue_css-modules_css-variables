<template>
  <footer>
    <div :class="$style['footer-content']">
      <img :class="$style['sculpture-image']" :src="footerSculpture" alt=" Sculpture image">
      <p :class="$style['footer-content-text']">Thanks for visit my website<br>If you have any questions you can write me to any of my social networks, I am sure I will answer you.</p>
    </div>
    <img width="73" height="27" :src="logo" alt="Logo" :class="$style.logo">
    <nav :class="$style.nav" aria-label="Footer menu">
      <ul :class="[$style['nav-list']]">
        <li><a href="#">Home</a></li>
        <li><a href="#portfolio">Portfolio</a></li>
        <li><a href="#skills">Skills</a></li>
        <li><a href="#about">About Me</a></li>
      </ul>
    </nav>
  </footer>
</template>

<script setup>
import logo from '@/assets/images/logo.png';
import footerSculpture from '@/assets/images/footer-sculpture.png';

</script>

<style lang="css" module>
footer {
  width: 100%;
  padding: 150px 22px 16px 22px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  gap: 40px;
  align-items: center;
  justify-content: space-between;
  background-color: var(--color-gray);
  position: relative;
}

.footer-content {
  position: absolute;
  top: 0;
  transform: translateY(-40%);
  width: calc(100% - 44px);
  padding: 20px 20px 20px 50%;
  border-radius: 15px;
  background-color: var(--color-purple-dark);
  box-sizing: border-box;
}

.nav {
  display: flex;
}

.nav-list {
  display: flex;
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.nav-list a {
  display: block;
  text-decoration: none;
  font-size: 11px;
  color: var(--color-white);
  font-weight: 300;
  padding: 8px 16px;
  border-radius: 4px;
}

.nav-list a:hover {
  background-color: var(--color-purple-dark);
}

.sculpture-image {
  width: 150px;
  position: absolute;
  bottom: 0;
  left: 0;
}

.footer-content-text {
  font-weight: 500;
  line-height: 16px;
  font-size: 12px;
}

@media screen and (min-width: 640px) {
  footer {
    flex-direction: row;
  }

  .footer-content {
    width: calc(100% - 44px);
    padding: 20px 20px 20px 27%;
  }

  .sculpture-image {
    width: 160px;
  }

  .footer-content-text {
    line-height: 20px;
    font-size: 14px;
  }

  .nav-list {
    gap: 5px;
  }

  .nav-list a {
    font-size: 18px;
  }
}

@media screen and (min-width: 1024px) {
  footer {
    padding: 150px 60px 30px 60px;
  }

  .footer-content {
    width: calc(100% - 120px);
    padding: 40px 20px 40px 20%;
  }

  .sculpture-image {
    width: 180px;
  }

  .footer-content-text {
    line-height: 24px;
    font-size: 15px;
  }
}

@media screen and (min-width: 1536px) {
  footer {
    padding: 150px 80px 30px 80px;
  }

  .footer-content {
    width: calc(100% - 160px);
    padding: 70px 20px 70px 20%;
  }

  .sculpture-image {
    width: 250px;
  }
}
</style>
