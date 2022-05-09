<template>
  <div class="card-item" :class="{ show: !isClamped }">
    <div class="card-header">
      <img src="../../public/icons/exclaim.png" alt="exclaim icon" />
    </div>
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <p v-html="description" :class="{ clamp: isClamped }"></p>
      <span class="img-container" @click="isClamped = !isClamped">
        <img
          v-if="!isClamped"
          src="../../public/icons/minus.png"
          alt="minus icon"
        />
        <img v-else src="../../public/icons/plus.png" alt="plus icon" />
      </span>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
  name: "CardItem",
  data() {
    return {
      isClamped: true,
    };
  },
};
</script>
<style lang="scss" scoped>

.card-item {
  max-width: 354px;
  width: 100%;
  margin-left: 15px;
  margin-right: 15px;
  margin-bottom: 32px;

  .card-header {
    padding: 37px 0;
    background: $gray-100;
    border-top-right-radius: 5px;
    border-top-left-radius: 5px;

    img {
      height: 27px;
    }
  }

  .card-body {
    background: $black;
    font-size: 19px;
    padding: 28px 30px 19px;

    h5 {
      font-size: 15px;
      margin-bottom: 11px;
    }

    p {
      line-height: 1.2;
      max-width: 267px;
      margin: 0 auto;
      text-align: center;

      &.clamp {
        max-height: 45px;
        overflow: hidden;
      }
    }

    .img-container {
      background: $dark;
      padding: 2.75px 12px;
      border-radius: 50%;
      margin-top: 15px;
      display: inline-block;
      cursor: pointer;
    }
  }

  &.show {
    .img-container {
      margin-top: 25px;
      margin-bottom: 12px;
    }
  }
}
</style>