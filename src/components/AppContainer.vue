<template>
  <div
    class="
      app-container
      d-flex
      align-items-center
      justify-content-around
      flex-column
      text-center
    "
    :style="{ height: containerHeight + 'px', width: containerWidth + 'px' }"
  >
    <input
      class="app-input"
      :value="inputVal"
      @keypress="onlyNumber"
      @blur="updateInput"
      :disabled="disableInput"
    />
    <img class="app-img" alt="gear icon" :src="getImgUrl()" />
    <h6 class="app-text">{{ text }}</h6>
  </div>
</template>
<script>
import { bus } from "../main";

export default {
  name: "AppContainer",
  props: {
    text: {
      type: String,
    },
    icon: {
      type: String,
    },
    inputVal: {
      type: [String, Number],
    },
    containerHeight: {
      default: "120",
    },
    containerWidth: {
      default: "120",
    },
    disableInput: {
      default: false,
    },
    type: {
      type: String,
      required: true,
    },
  },
  methods: {
    getImgUrl() {
      return require("@/assets/" + `${this.icon}-icon.png`);
    },
    onlyNumber($event) {
      //console.log($event.keyCode); //keyCodes value
      let keyCode = $event.keyCode ? $event.keyCode : $event.which;
      if (keyCode < 48 || keyCode > 57) {
        $event.preventDefault();
      }
    },
    updateInput(val) {
      bus.$emit("update-input", {
        type: this.type,
        value: val.target.value,
      });
    },
  },
};
</script>