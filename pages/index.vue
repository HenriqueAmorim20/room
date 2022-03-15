<template>
  <div class="main">
    <div class="top">
      <section class="top-main-img">
        <v-img :src="require(`@/static/desktop-image-hero-${index+1}.jpg`)" contain />
      </section>
      <aside class="desc-section">
        <h1 class="desc-section-title">{{ heroes[index].title }}</h1>
        <p class="desc-section-info">
          {{ heroes[index].desc }}
        </p>
        <v-btn class="desc-section-btn">
          <span> shop now </span>
          <v-img
            class="desc-section-btn-icon"
            :src="require('@/static/icon-arrow.svg')"
          />
        </v-btn>
        <div class="desc-section-actions">
          <v-img
            class="desc-section-actions-arrow"
            :src="require('@/static/icon-angle-left.svg')"
            @click="changeContent(1)"
          />
          <v-img
            class="desc-section-actions-arrow"
            :src="require('@/static/icon-angle-right.svg')"
            @click="changeContent(-1)"
          />
        </div>
      </aside>
    </div>
    <div class="bottom">
      <aside class="side-img">
        <v-img :src="require('@/static/image-about-dark.jpg')" contain />
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
        <v-img :src="require('@/static/image-about-light.jpg')" contain />
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
      this.index += i
      if(this.index < 0) this.index = this.heroes.length -1
      else if(this.index === this.heroes.length) this.index = 0
    }
  }
};
</script>

<style scoped>
.main {
  height: 100vh;
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
}

.desc-section-actions {
  display: flex;
}

.desc-section-actions-arrow {
  max-width: 50px !important;
  aspect-ratio: 1 !important;
  background-color: #000;
  cursor: pointer;
}

.bottom {
  display: flex;
}

.side-img {
  width: 30%;
}

.about-section {
  width: 40%;
}
</style>
