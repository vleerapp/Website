<template>
  <NuxtPage />
</template>

<!-- <script>
export default {
  mounted() {
    this.$nextTick(() => {
      const locoScroll = new LocomotiveScroll({
        el: document.querySelector(".locomotive-scroll"),
        smooth: true,
        multiplier: 0.6,
      });

      setTimeout(() => {
        locoScroll.update();
      }, 2000);
    });
  },
};
</script> -->

<style lang="scss">
$background: #030303;
$small-text: #ababab;
$normal-text: #ffffff;
$card-outline: rgb(255 255 255 / .1);
$card-padding: .5rem;

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter';
  color: $normal-text;
}

@font-face {
  font-family: Inter;
  src: url("/Inter.woff2") format("woff2");
  font-display: swap;
}

@font-face {
  font-family: Maax;
  src: url("/Maax-Medium.woff") format("woff");
  font-display: swap;
}

@font-face {
  font-family: Maax-Regular;
  src: url("/Maax.woff") format("woff");
  font-display: swap;
}

html,
body {
  background-color: $background;
  scroll-behavior: cubic-bezier(0.42, 0, 0.58, 1);
  scroll-behavior: smooth;
}

a {
  text-decoration: none;
}
</style>
