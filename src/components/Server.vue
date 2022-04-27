<template>
  <AppContainer
    class="server-box"
    icon="server"
    text="Server"
    :inputVal="inputValue"
    type="server"
  />
</template>
<script>
import AppContainer from "@/components/AppContainer";
export default {
  name: "Server",
  props: ["inputValue"],
  components: { AppContainer },
};
</script>
<style lang="scss" scoped>
.server-box {
  position: absolute;
  transform: translate(-232%, -75%);
}
</style>