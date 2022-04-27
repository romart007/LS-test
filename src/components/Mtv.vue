<template>
  <AppContainer
    class="mtv-box"
    icon="mtv"
    text="MTV"
    :inputVal="inputValue"
    type="mtv"
  />
</template>
<script>
import AppContainer from "@/components/AppContainer";
export default {
  name: "Mtv",
  props: ["inputValue"],
  components: { AppContainer },
};
</script>
<style lang="scss" scoped>
.mtv-box {
  position: absolute;
  transform: translate(235%, 145%);
}
</style>