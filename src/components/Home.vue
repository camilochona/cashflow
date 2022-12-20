<template>
  <LayoutVue>
    <template #header> <HeaderVue></HeaderVue></template>
    <template #resume>
      <Resume></Resume>
    </template>
    <template #movements>
      <Movements></Movements>
    </template>
  </LayoutVue>
</template>

<script>
import LayoutVue from "./Layout.vue";
import HeaderVue from "./Header.vue";
import Resume from "./Resume/index.vue";
import Movements from "./Movements.vue";

export default {
  components: {
    LayoutVue,
    HeaderVue,
    Resume,
    Movements,
  },
};
</script>
