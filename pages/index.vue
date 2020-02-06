<template>
  <div class="container">
    <Header />
    <main class="main">
      <Vector />
      <Images />
      <Slider />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "~/components/header.vue";
import Vector from "~/components/vector.vue";
import Images from "~/components/images.vue";
import Slider from "~/components/slider.vue";
import Footer from "~/components/footer.vue";

export default {
  components: {
    Header,
    Vector,
    Images,
    Slider,
    Footer
  }
};
</script>

<style lang="less">
@font-face {
  font-family: "Travels";
  src: url(/fonts/TTTravels-Light.ttf) format("truetype");
  font-weight: 300;
  font-style: normal;
}
@font-face {
  font-family: "Cond";
  src: url(/fonts/Schnyder_X_Cond_XL_Demi.otf) format("opentype");
  font-weight: normal;
  font-style: normal;
}

a {
  height: fit-content;
  text-decoration: none;
}

.container {
  height: 100vh;
  cursor: url("/cursore.svg"), auto;
}


// @media only screen and (max-width: 1024px) {
//   .main {
//     height: 530px;
//   }
// }
</style>

