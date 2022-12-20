<template>
  <LayoutVue>
    <template #header> <HeaderVue></HeaderVue></template>
    <template #resume>
      <Resume
        :label="'Ahorro Total'"
        :amount="amount"
        :total-amount="1000000"
        :dateLabel="dateLabel"
      >
        <template #graphic>Graphic</template>
        <template #action>Action</template>
      </Resume>
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
  data() {
    return {
      amount: null,
      dateLabel: "22/10/2022",
    };
  },
};
</script>
