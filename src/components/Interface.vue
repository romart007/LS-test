<template>
  <AppContainer
    class="int-box"
    icon="int"
    text="Interface"
    :inputVal="inputValue"
    type="interface"
  />
</template>
<script>
import AppContainer from "@/components/AppContainer";
export default {
  props: ["inputValue"],
  name: "Interface",
  components: { AppContainer },
};
</script>
<style lang="scss" scoped>
.int-box {
  position: absolute;
  transform: translate(0%, -212%);
}
</style>