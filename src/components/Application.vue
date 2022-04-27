<template>
  <AppContainer
    class="app"
    icon="app"
    text="Application"
    type="application"
    :inputVal="inputValue"
    containerHeight="200"
    containerWidth="200"
    :disableInput="true"
  />
</template>
<script>
import AppContainer from "@/components/AppContainer";
export default {
  name: "Applications",
  components: { AppContainer },
  props: {
    inputValue: {
      type: [String, Number],
      default: 0,
    },
  },
};
</script>
<style lang="scss">
.app {
  margin-top: 94px;
}
</style>