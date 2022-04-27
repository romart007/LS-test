<template>
  <AppContainer
    class="app-grp-box"
    icon="app-grp"
    text="App Group"
    :inputVal="inputValue"
    type="appGroup"
  />
</template>
<script>
import AppContainer from "@/components/AppContainer";
export default {
  name: "AppGroup",
  props: ["inputValue"],
  components: { AppContainer },
};
</script>
<style lang="scss" scoped>
.app-grp-box {
  position: absolute;
  transform: translate(-232%, 145%);
}
</style>