<template>
  <AppContainer
    class="func-box"
    icon="func"
    text="functions"
    :inputVal="inputValue"
    type="funcs"
  />
</template>
<script>
import AppContainer from "@/components/AppContainer";
export default {
  name: "Functions",
  props: ["inputValue"],
  components: { AppContainer },
};
</script>
<style lang="scss" scoped>
.func-box {
  position: absolute;
  transform: translate(0%, 290%);
}
</style>