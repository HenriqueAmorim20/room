<template>
  <div class="main">
    <div class="top">
      <section class="main-img">
        <v-img :src="require('@/static/desktop-image-hero-1.jpg')" />
      </section>
      <aside class="desc-section">
        <h1 class="desc-section-title">{{ heroes[index].title }}</h1>
        <p class="desc-section-info">
          {{ heroes[index].desc }}
        </p>
        <v-btn class="desc-section-btn">
          <span> shop now </span>
          <v-img :src="require('@/static/icon-arrow.svg')" />
        </v-btn>
        <div class="desc-section-actions">
          <v-img :src="require('@/static/icon-angle-left.svg')" />
          <v-img :src="require('@/static/icon-angle-right.svg')" />
        </div>
      </aside>
    </div>
    <div class="bottom">
      <aside class="side-img">
        <v-img :src="require('@/static/image-about-dark.jpg')" />
      </aside>
      <section class="about-section">
        <h2 class="about-section-title">About our furniture</h2>
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
};
</script>

<style scoped>
.main {
  min-height: 100vh;
}
</style>
