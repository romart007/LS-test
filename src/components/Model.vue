<template>
  <Main>
    <b-container
      class="main-container d-flex align-items-center justify-content-center"
    >
      <Interface :inputValue="appData.interface" />
      <svg class="int-line" width="500" height="500" style="position: absolute">
        <line
          data-v-76ee2aa9=""
          x1="210"
          y1="55"
          x2="210"
          y2="196"
          stroke="black"
        ></line>
      </svg>
      <svg class="int-line" width="500" height="500" style="position: absolute">
        <line
          data-v-76ee2aa9=""
          x1="290"
          y1="55"
          x2="290"
          y2="196"
          stroke="black"
        ></line>
      </svg>
      <Server :inputValue="appData.server" />
      <svg
        data-v-76ee2aa9=""
        width="500"
        height="400"
        class="server-short-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="32"
          y1="100"
          x2="62"
          y2="100"
          stroke="black"
        ></line>
      </svg>
      <svg
        data-v-76ee2aa9=""
        width="400"
        height="400"
        class="server-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="12"
          y1="100"
          x2="70"
          y2="200"
          stroke="black"
        ></line>
      </svg>
      <svg
        data-v-76ee2aa9=""
        width="400"
        height="400"
        class="server-short-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="70"
          y1="200"
          x2="100"
          y2="200"
          stroke="black"
        ></line>
      </svg>
      <AppGroup :inputValue="appData.appGroup" />
      <svg
        data-v-76ee2aa9=""
        width="500"
        height="400"
        class="appgrp-short-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="32"
          y1="375"
          x2="62"
          y2="375"
          stroke="black"
        ></line>
      </svg>
      <svg
        data-v-76ee2aa9=""
        width="400"
        height="400"
        class="appgrp-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="12"
          y1="375"
          x2="70"
          y2="275"
          stroke="black"
        ></line>
      </svg>
      <svg
        data-v-76ee2aa9=""
        width="400"
        height="400"
        class="appgrp-short-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="70"
          y1="275"
          x2="100"
          y2="275"
          stroke="black"
        ></line>
      </svg>
      <Application :inputValue="applicationTotal" />
      <Mtv :inputValue="appData.mtv" />
      <svg
        data-v-76ee2aa9=""
        width="500"
        height="400"
        class="mtv-short-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="442"
          y1="375"
          x2="472"
          y2="375"
          stroke="black"
        ></line>
      </svg>
      <svg
        data-v-76ee2aa9=""
        width="500"
        height="400"
        class="mtv-line"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="380"
          y1="275"
          x2="442"
          y2="375"
          stroke="black"
        ></line>
      </svg>
      <svg
        data-v-76ee2aa9=""
        width="500"
        height="400"
        class="mtv-short-line"
        style="position: absolute; z-index: 500"
      >
        <line
          data-v-76ee2aa9=""
          x1="350"
          y1="275"
          x2="380"
          y2="275"
          stroke="black"
        ></line>
      </svg>
      <Funcs :inputValue="appData.funcs" />
      <svg
        class="func-line"
        data-v-76ee2aa9=""
        width="500"
        height="600"
        style="position: absolute"
      >
        <line
          data-v-76ee2aa9=""
          x1="250"
          y1="446"
          x2="251"
          y2="580"
          stroke="black"
        ></line>
      </svg>
    </b-container>
  </Main>
</template>
<script>
import Main from "@/layouts/Main";
import Application from "@/components/Application";
import Interface from "@/components/Interface";
import Server from "@/components/Server";
import AppGroup from "@/components/AppGroup";
import Mtv from "@/components/Mtv";
import Funcs from "@/components/Funcs";
import { bus } from "../main";

export default {
  components: { Main, Application, Interface, Server, AppGroup, Mtv, Funcs },
  data() {
    return {
      appData: {
        interface: 223,
        server: 55,
        appGroup: 66,
        mtv: 224,
        funcs: 130,
      },
    };
  },
  methods: {
    updateAppData(val, type) {
      this.appData[type] = +val;
    },
  },
  computed: {
    applicationTotal() {
      return Object.values(this.appData).reduce(
        (a, b) => Number(a) + Number(b),
        0
      );
    },
  },
  created() {
    bus.$on("update-input", (data) => {
      this.updateAppData(data.value || 0, data.type);
    });
  },
};
</script>
<style lang="scss" scoped>
.main-container {
  height: 115vh;
}
</style>