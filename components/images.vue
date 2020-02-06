<template>
  <div class="images" ref="imagesHeight">
    <img src="/image1.png" alt />
    <img src="/image2.png" alt />
    <img src="/image3.png" alt />
    <span v-bind:style="mainHeight"></span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mainHeight: {}
    };
  },
  methods: {
    matchHeight() {
      var heightString = this.$refs.imagesHeight.clientHeight + "px";
      // Vue.set(this.mainHeight, "height", heightString);
      console.log(heightString);
    }
  },
  mounted() {
    this.matchHeight();
  }
};
</script>

<style lang="less">
.images {
  display: flex;
  justify-content: center;
  width: fit-content;
  margin: auto;
  position: absolute;
  top: -50px;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  height: fit-content;

  img {
    object-fit: fill;

    &:nth-child(1) {
      width: 238px;
      height: 331px;
      margin-top: 125px;
    }
    &:nth-child(2) {
      width: 476px;
      height: 702px;
      margin-left: 5.75px;
    }
    &:nth-child(3) {
      align-self: flex-end;
      margin-bottom: 43px;
      margin-left: -77px;
    }
  }
}

@media only screen and (max-width: 1024px) {
  .images {
    top: -40px;
    img {
      &:nth-child(1) {
        width: 163px;
        height: 226px;
        margin-top: 125px;
      }
      &:nth-child(2) {
        width: 359px;
        height: 530px;
        margin-left: 5.75px;
      }
      &:nth-child(3) {
        align-self: flex-end;
        width: 234px;
        margin-bottom: 43px;
        margin-left: -77px;
      }
    }
  }
}

@media only screen and (max-width: 414px) {
  .images {
    top: -40px;
    img {
      &:nth-child(1) {
        display: none;
      }
      &:nth-child(2) {
        width: 273px;
        height: 403px;
        margin-left: 0;
      }
      &:nth-child(3) {
        display: none;
      }
    }
  }
}
@media only screen and (max-width: 375px) {
  .images {
    top: -40px;
    img {
      &:nth-child(2) {
        width: 249px;
        height: 368px;
        margin-left: 0;
      }
    }
  }
}
</style>