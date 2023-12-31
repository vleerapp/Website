<template>
  <NuxtLayout>
    <div class="hero">
      <h1 class="title">A Music app from the Future</h1>
      <h2 class="description">
        Discover a redefined way of listing to music, all conveniently
        accessible right at your fingertips
      </h2>
      <Download />
    </div>
    <div id="hero-img-container" class="hero-img-container">
      <nuxt-img
        src="/hero.webp"
        alt="hero"
        id="hero-image"
        class="hero-image"
        quality="80"
        densities="x1 x2"
      />
    </div>
    <div class="cards">
      <h3 class="cards-text">
        Superchare your experience with the features of Vleer
      </h3>
      <div class="card-grid">
        <div class="card">
          <div class="soundwave3"></div>
          <div class="text">Full Control</div>
          <p class="card-description">
            Have full control over what you listen to and also over the data
            that is not collected about you. Privacy first!
          </p>
          <nuxt-img
            src="/fullcontrol.svg"
            class="card-icon"
            alt=""
            loading="lazy"
          />
        </div>
        <div class="card">
          <div class="soundwave2"></div>
          <div class="text">Thank you for choosing us</div>
          <div class="soundwave1"></div>
        </div>
        <div class="card">
          <div class="text">Offline</div>
          <p class="card-description">
            Enjoy Music completly offline thanks to the serverless system we
            developed.
          </p>
          <nuxt-img
            src="/offline.svg"
            class="card-icon"
            alt=""
            loading="lazy"
          />
        </div>
        <div class="card">
          <div class="text">Completly Free</div>
          <p class="card-description">
            Vleer is 100% free and this will stay like this as long as Vleer is
            in our charge.
          </p>
          <nuxt-img src="/free.svg" class="card-icon" alt="" loading="lazy" />
        </div>
        <div class="card">
          <div class="soundwave1"></div>
          <div class="text">Search</div>
          <p class="card-description">
            Search with our powerfull search bar through a land full of Music to
            enjoy.
          </p>
          <nuxt-img src="/search.svg" class="card-icon" alt="" loading="lazy" />
        </div>
      </div>
    </div>
    <Ready />
  </NuxtLayout>
</template>

<script setup lang="ts">
useSeoMeta({
  title: "Vleer - A Music app from the Future",
  description:
    "Discover a redefined way of listing to music, all conveniently accessible right at your fingertips",
  ogTitle: "Vleer - A Music app from the Future",
  ogDescription:
    "Discover a redefined way of listing to music, all conveniently accessible right at your fingertips",
  ogImage: "/logo.webp",
  ogUrl: "https://vleer.app",
  twitterTitle: "Vleer - A Music app from the Future",
  twitterDescription:
    "Discover a redefined way of listing to music, all conveniently accessible right at your fingertips",
  twitterImage: "/logo.webp",
  twitterCard: "summary",
});

useHead({
  htmlAttrs: {
    lang: "en",
  },
  link: [
    {
      rel: 'canonical',
      href: 'https://vleer.app',
    },
    {
      rel: "icon",
      type: "image/ico",
      href: "/favicon.ico",
    },
  ],
});
</script>

<style lang="scss">
.title {
  font-family: Maax;
  font-size: 64px;
  max-width: 600px;
  text-align: center;
  line-height: 60px;
}

.description {
  color: #ababab;
  font-size: 16px;
  font-weight: normal;
  margin-top: 24px;
  margin-bottom: 32px;
  max-width: 370px;
  text-align: center;
}

.hero {
  align-items: center;
  justify-content: center;
  display: flex;
  flex-direction: column;
  margin-bottom: 100px;
  padding-top: 180px;
  width: 100%;
}

.hero-image {
  max-width: 1185px;
  height: 690px;
  width: 1185px;
  outline: 1px solid #544d5e6b;
  outline-offset: 8px;
  border-radius: 22px;
}

@media (max-width: 1248px) {
  .hero-image {
    height: calc((46 / 79) * (100vw - 64px));
    width: calc(100vw - 64px);
  }
}

.hero-img-container {
  margin-inline: 8px;
}

.cards {
  padding-top: 180px;
  max-width: 1200px;
  height: auto;
  width: 100%;
  border-radius: 22px;
  display: grid;
  justify-items: center;

  .cards-text {
    max-width: 900px;
    text-align: center;
    font-size: 50px;
    margin-bottom: 80px;
  }

  .card-grid {
    width: 1200px;
    height: 572px;
    display: grid;
    gap: 24px;
    grid-template-rows: 274px 274px;
    grid-template-columns: 384px 384px 384px;
    place-items: center;

    .card {
      position: relative;
      outline: 1px solid #544d5e6b;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      gap: 8px;
      padding: 34px;
      padding-bottom: 0 !important;
      border-radius: 24px;
      font-size: 30px;

      .text {
        /* margin-left: -40px;
        margin-top: -40px; */
        max-width: 80%;
        z-index: 1;
        font-size: 26px;
      }

      .card-icon {
        width: 50px;
        align-self: center;
        z-index: 1;
        position: absolute;
        bottom: 34px;
      }

      .card-description {
        font-size: 16px;
        color: #ababab;
        z-index: 1;
      }

      &:nth-child(2) {
        grid-column: 2 / 3;
        grid-row: 1 / 3;
        font-size: 45px;
        text-align: center;
        justify-content: center;
        align-items: center;
        padding: 0;

        .text {
          margin-left: 0px;
          margin-top: 0px;
          max-width: 80%;
          font-size: 44px;
        }
      }
    }
  }
}

@media (min-width: 1248px) {
  .card:nth-child(1) {
    background-image: url("/card1.webp");
  }

  .card:nth-child(2) {
    background-image: url("/card3.webp");
  }

  .card:nth-child(3) {
    background-image: url("/card4.webp");
  }

  .card:nth-child(4) {
    background-image: url("/card2.webp");
  }

  .card:nth-child(5) {
    background-image: url("/card5.webp");
  }
}

@media (max-width: 1248px) {
  .card-grid {
    width: 100% !important;
    height: 870px !important;
    grid-template-rows: 274px 274px 274px !important;
    grid-template-columns: calc(50% - 12px) calc(50% - 12px) !important;
  }

  .card {
    background-size: cover;
    overflow: hidden;
  }

  .soundwave1 {
    width: 274px;
    position: absolute;
    background-image: url("/sound-wave.webp");
    background-size: 385px;
    background-repeat: no-repeat;
    height: 100%;
    right: 0;
    top: 0;
    z-index: 0;
    background-position: 70px 64px !important;

    &:nth-child(1) {
      background-position: 70px -236px !important;
    }

    &:nth-child(2) {
      background-position: 70px 64px !important;
    }
  }

  .soundwave3 {
    width: 274px;
    position: absolute;
    background-image: url("/sound-wave.webp");
    background-size: 385px;
    background-repeat: no-repeat;
    height: 100%;
    left: 0;
    top: 0;
    z-index: 0;
    rotate: 180deg;
    background-position: 80px -230px;
  }

  .soundwave2 {
    width: 274px;
    position: absolute;
    background-image: url("/sound-wave.webp");
    background-size: 385px;
    background-repeat: no-repeat;
    height: 100%;
    left: 0;
    top: 0;
    z-index: 0;
    rotate: 180deg;
    background-position: 80px 70px;
  }

  .card:nth-child(1) {
    grid-row: 1/1 !important;
    grid-column: 1/1 !important;
    background-image: url("/card1-half.webp");
  }

  .card:nth-child(2) {
    grid-row: 2/2 !important;
    grid-column: 1/3 !important;
    background-image: url("/card3-half.webp");

    .text {
      width: 400px;
    }
  }

  .card:nth-child(3) {
    grid-row: 1/1 !important;
    grid-column: 2/2 !important;
    background-image: url("/card4-half.webp");
  }

  .card:nth-child(4) {
    background-image: url("/card2-half.webp");
  }

  .card:nth-child(5) {
    background-image: url("/card5-half.webp");
  }
}

@media (max-width: 900px) {
  .cards {
    padding-top: 100px;
  }

  .soundwave1 {
    background-size: 300px;
    background-position: 130px 130px !important;

    &:nth-child(1) {
      display: none;
    }
  }

  .soundwave3 {
    display: none;
  }

  .soundwave2 {
    background-size: 300px;
    background-position: 130px 130px;
  }

  .card-grid {
    height: 1468px !important;
    grid-template-rows: repeat(274px, 5) !important;
    grid-template-columns: 100% !important;

    .card {
      height: 274px !important;
      grid-column: 1/2 !important;
      grid-row: auto !important;

      &:nth-child(2) {
        .text {
          font-size: 32px;
          max-width: 290px !important;
          font-weight: 500;
        }
      }
    }
  }
}

@media (max-width: 1000px) {
  .hero-image {
    border-radius: 10px;
  }
}

@media (max-width: 700px) {
  .title {
    font-size: 48px;
    line-height: 50px;
  }

  .hero {
    padding-top: 80px;
  }

  .hero-image {
    outline-offset: 6px;
    border-radius: 10px;
  }

  .text {
    font-size: 20px;
  }

  .cards-text {
    font-size: 32px !important;
    max-width: 500px !important;
    margin-bottom: 48px !important;
  }
}
</style>
