<template>
  <div class="main">
    <div class="top">
      <section class="top-main-img">
        <v-img :src="require(`@/static/desktop-image-hero-${index + 1}.jpg`)" contain/>
      </section>
      <aside class="desc-section">
        <h1 class="desc-section-title">{{ heroes[index].title }}</h1>
        <p class="desc-section-info">
          {{ heroes[index].desc }}
        </p>
        <div class="desc-section-btn">
          <span> shop now </span>
          <v-img
            class="desc-section-btn-icon"
            :src="require('@/static/icon-arrow.svg')"
          />
        </div>
        <div class="desc-section-actions">
          <div class="desc-section-actions-arrow" @click="changeContent(-1)">
            <v-img :src="require('@/static/icon-angle-left.svg')" />
          </div>
          <div class="desc-section-actions-arrow" @click="changeContent(1)">
            <v-img :src="require('@/static/icon-angle-right.svg')" />
          </div>
        </div>
      </aside>
    </div>
    <div class="bottom">
      <aside class="side-img">
        <v-img :src="require('@/static/image-about-dark.jpg')" />
      </aside>
      <section class="about-section">
        <h5 class="about-section-title">About our furniture</h5>
        <p class="about-section-info">
          Our multifunctional collection blends design and function to suit your
          individual taste. Make each room unique, or pick a cohesive theme that
          best express your interests and what inspires you. Find the furniture
          pieces you need, from traditional to contemporary styles or anything
          in between. Product specialists are available to help you create your
          dream space.
        </p>
      </section>
      <aside class="side-img">
        <v-img :src="require('@/static/image-about-light.jpg')" />
      </aside>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      heroes: [
        {
          title: "Discover innovative ways to decorate",
          desc: "We provide unmatched quality, comfort, and style for property owners across the country. Our experts combine form and function in bringing your vision to life. Create a room in your own style with our collection and make your property a reflection of you and what you love.",
        },
        {
          title: "We are available all across the globe",
          desc: "With stores all over the world, it's easy for you to find furniture for your home or place of business.  Locally, we’re in most major cities throughout the country. Find the branch nearest you using our store locator. Any questions? Don't hesitate to contact us today.",
        },
        {
          title: "Manufactured with the best materials",
          desc: "Our modern furniture store provide a high level of quality. Our company has invested in advanced technology to ensure that every product is made as perfect and as consistent as possible. With three decades of experience in this industry, we understand what customers want for their home and office.",
        },
      ],
      index: 0,
    };
  },
  methods: {
    changeContent(i) {
      this.index += i;
      if (this.index < 0) this.index = this.heroes.length - 1;
      if (this.index === this.heroes.length) this.index = 0;
    },
  },
};
</script>

<style scoped>
.main {
  display: flex;
  flex-direction: column;
}

.top {
  display: flex;
}

.top-main-img {
  width: 60%;
}

.desc-section {
  width: 40%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  max-width: 650px;
  position: relative;
  padding: min(5%, 5.5rem);
}

.desc-section-title {
  font-size: clamp(1rem,2.5vw,2.3rem);
  line-height: 35px;
}

.desc-section-info {
  font-size: clamp(0.6rem,1vw,0.9rem);
  color: var(--DarkGray);
  margin: 2rem 0;
}

.desc-section-btn {
  display: flex;
  align-items: center;
  text-transform: uppercase;
  cursor: pointer;
  color: var(--Black);
  font-weight: 500;
  font-size: clamp(0.6rem,1vw,0.9rem);
  letter-spacing: 0.5vw;
  transition: opacity 0.5s ease;
}

.desc-section-btn-icon {
  max-width: min(50px, 3vw) !important;
  margin-left: 40px;
  transition: transform 0.7s ease;
}

.desc-section-btn:hover {
  opacity: 0.5;
}

.desc-section-btn:hover .desc-section-btn-icon {
  transform: translate(10px, 0);
}

.desc-section-actions {
  display: flex;
  position: absolute;
  bottom: 0;
  left: 0;
}

.desc-section-actions-arrow {
  display: flex;
  align-items: center;
  justify-content: center;
  aspect-ratio: 1;
  background-color: #000;
  cursor: pointer;
  padding: 1vw 2vw;
  transition: opacity 0.5s ease;
}

.desc-section-actions-arrow:hover {
  opacity: 0.75;
}

.bottom {
  display: flex;
}

.about-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: min(4vw,3rem);
}

.about-section-title {
  text-transform: uppercase;
  letter-spacing: 6px;
  font-size: clamp(0.7rem,1vw,1rem);
}

.about-section-info {
  font-size: clamp(0.6rem,1vw,0.9rem);
  color: var(--DarkGray);
  margin: 1rem 0 0;
}

.side-img {
  width: 30%;
}

.about-section {
  width: 40%;
}
</style>
