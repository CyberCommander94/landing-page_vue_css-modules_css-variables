<template>
  <section id="about" :class="$style['about-section']">
    <div :class="$style.cell1">
      <div :class="$style['about-title-wrapper']">
        <h3 :class="$style['about-title']">ABOUT ME</h3>
        <img :class="$style['about-zig-zag']" :src="zigZagLine" alt="Zig zag line">
      </div>
      <p :class="[$style['about-text'], $style['first']]">I am a <span :class="$style['first-block-gradient']">Product Designer</span> and Frontend Developer, I fully understand the process of design and development of a digital product, my job is to make a product usable and visually appealing, through the <span :class="$style['first-block-gradient']">Design Thinking</span> methodology I manage to create products that are endearing to users.</p>
    </div>
    <div :class="$style.cell2">
      <img :class="$style['about-image']" :src="photo1" alt="Photo 1">
    </div>
    <div :class="$style.cell3">
      <img :class="$style['about-image']" :src="photo2" alt="Photo 2">
    </div>
    <div :class="$style.cell4" style="display: flex; align-items: center;">
      <p :class="[$style['about-text'], $style['second']]">I am passionate about <span :class="$style['second-block-gradient']">never stop</span> learning, I am constantly training and <span :class="$style['second-block-gradient']">learning</span> about new and changing <span :class="$style['second-block-gradient']">technology</span> trends that way I bring an updated opinion of the Tech industry.</p>
    </div>
    <div :class="$style.cell5" style="display: flex; align-items: center;">
      <p :class="[$style['about-text'], $style['third']]">My full name is <span :class="$style['third-block-gradient']">Cristian David Muñoz Camayo</span> and more than what I said before I am a dreamer, I am proudly <span :class="$style['colombia-gradient']">Colombian</span> and in me you will find a human being with the desire to do his best to help others.</p>
    </div>
    <div :class="$style.cell6">
      <img :class="$style['about-image']" :src="photo3" alt="Photo 3">
    </div>
  </section>
</template>

<script setup>
import zigZagLine from '@/assets/images/zig-zag-line.png';
import photo1 from '@/assets/images/photo1.png';
import photo2 from '@/assets/images/photo2.png';
import photo3 from '@/assets/images/photo3.png';

</script>

<style lang="css" module>
.about-section {
  width: 100%;
  display: grid;
  grid-template-rows: repeat(6, auto);
  grid-template-columns: 1fr;
  padding: 100px 22px 160px 22px;
}

.about-image {
  width: 100%;
  height: auto;
  object-fit: cover;
  display: block;
  height: 100%;
}

.about-title {
  font-family: var(--font-family-secondary);
  font-weight: 100;
  margin: 0;
  font-size: 64px;
}

.about-zig-zag {
  display: none;
}

.about-text {
  font-weight: 700;
  font-size: 22px;
  margin-bottom: 40px;
  margin-top: 40px;
}

.first-block-gradient {
  background-image: linear-gradient(to right, #FA709A, #FEE140);
  color: transparent;
  background-clip: text;
}

.second-block-gradient {
  background-image: linear-gradient(to right, #65C8FF, lightgreen);
  color: transparent;
  background-clip: text;
}

.third-block-gradient {
  background-image: linear-gradient(to right, rgb(251, 183, 251), rgb(176, 176, 235));
  color: transparent;
  background-clip: text;
}

.colombia-gradient {
  background-image: linear-gradient(to right, #FFE76A 20%, #65C8FF 23%, #65C8FF 50%, #65C8FF 72%, #FF0000 72%);
  color: transparent;
  background-clip: text;
}

.cell1 {
  order: 1;
}

.cell2 {
  order: 2;
}

.cell3 {
  order: 4;
}

.cell4 {
  order: 3;
}

.cell5 {
  order: 5;
}

.cell6 {
  order: 6;
}


@media screen and (min-width: 640px) {
  .about-section {
    grid-template-rows: repeat(3, auto);
    grid-template-columns: repeat(2, 1fr);
    padding: 100px 22px 160px 22px;
  }

  .about-title-wrapper {
    display: flex;
    gap: 38px;
    align-items: center;
    padding: 0 0 20px 0;
  }

  .about-title {
    font-size: 44px;
  }

  .about-text {
    font-size: 16px;
  }

  .first,
  .third {
    margin: 0 36px 0 0;
  }

  .first {
    margin-bottom: 10px;
  }

  .second {
    margin: 0 0 0 36px;
  }

  .cell1,
  .cell2,
  .cell3,
  .cell4,
  .cell5,
  .cell6 {
    order: 0;
  }
}

@media screen and (min-width: 1024px) {
  .about-section {
    padding: 200px 80px 280px 80px;
  }

  .about-title {
    font-size: 64px;
  }

  .about-zig-zag {
    height: 20px;
    display: block;
    width: 30%;
  }

  .about-text {
    font-size: 20px;
  }

  .first,
  .third {
    margin: 0 72px 0 0;
  }

  .second {
    margin: 0 0 0 72px;
  }

  .about-title-wrapper {
    padding: 0 0 20px 0;
  }
}

@media screen and (min-width: 1536px) {
  .about-section {
    padding: 200px 80px 315px 80px;
  }

  .about-zig-zag {
    height: 30px;
  }

  .about-text {
    font-size: 36px;
  }

  .about-title-wrapper {
    padding: 0 0 30px 0;
  }
}
</style>
