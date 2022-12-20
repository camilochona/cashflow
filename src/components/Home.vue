<template>
  <LayoutVue>
    <template #header> <HeaderVue></HeaderVue></template>
  </LayoutVue>
</template>

<script>
import LayoutVue from "./Layout.vue";
import HeaderVue from "./Header.vue";
export default {
  components: {
    LayoutVue,
    HeaderVue,
  },
};
</script>
