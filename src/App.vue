<template>
  <div id="app">
    <Model />
  </div>
</template>

<script>
import Model from "@/components/Model";

export default {
  name: "App",
  components: {
    Model,
  },
};
</script>

<style lang="scss">
@import "~@/assets/scss/vendors/bootstrap-vue/index";
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap");

body {
  font-family: "Roboto", sans-serif;
  background: #e5e5e5;
}

.app-container {
  width: 120px;
  height: 120px;
  background: #ffffff;
  position: relative;
  border: 1px solid #e6eaf2;
  box-sizing: border-box;
  box-shadow: 0px 4px 4px rgba(46, 56, 77, 0.02);
  border-radius: 5px;

  /* Hover */
  &:hover,
  &:focus,
  &:active {
    border: 1px solid #e6eaf2;
    box-sizing: border-box;
    box-shadow: 0px 4px 4px rgba(46, 56, 77, 0.02);
    border-radius: 5px;
  }

  .app {
    &-input {
      text-align: center;
      font-size: 12px;
      line-height: 150%;
      color: #8a8e99;
      border-radius: 5px;
      border: 0 none;
      outline: 0 none;
      background: #e6eaf2;
      border-radius: 5px;
      height: 20px;
      width: 30px;
      border-radius: 5px;
      position: absolute;
      top: -11px;
    }

    &-img {
      max-height: 52.5px;
      max-width: 52.5px;
      margin-bottom: -20%;
    }
    &-text {
      /* Title */
      font-family: "Roboto";
      font-style: normal;
      font-weight: 400;
      font-size: 14px;
      line-height: 16px;
      text-align: center;

      /* Dark */
      color: #2e384d;
    }
  }
}
</style>
