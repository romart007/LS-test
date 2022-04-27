<template>
  <main class="main">
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