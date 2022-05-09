<template>
  <div id="app">
    <CardList />
  </div>
</template>

<script>
import CardList from "@/components/CardList";

export default {
  name: "App",
  components: {
    CardList,
  },
};
</script>

<style lang="scss">
@import "~@/assets/scss/vendors/bootstrap-vue/index";
@import "~@/assets/scss/_font.scss";

body {
  font-family: "ProximaNova-Regular", Arial, sans-serif;
  background: $dark;
  color: $gray-200;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Gotham-Bold", Arial, sans-serif;
  color: $white;
}
</style>
