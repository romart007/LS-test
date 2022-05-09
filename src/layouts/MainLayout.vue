<template>
  <main class="container">
    <slot></slot>
  </main>
</template>

<script>
export default {
  name: "MainWrapper",
  props: {
    msg: String,
  },
};
</script>
<style lang="scss">
@import "~@/assets/scss/mixins.scss";

.container {
  @include extra-small {
    padding-right: 20px;
    padding-left: 20px;
  }
}
</style>