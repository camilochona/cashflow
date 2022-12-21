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
      <Movements :movements="movements"></Movements>
    </template>
  </LayoutVue>
</template>

<script>
import LayoutVue from "./Layout.vue";
import HeaderVue from "./Header.vue";
import Resume from "./Resume/index.vue";
import Movements from "./Movements/index.vue";

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
      movements: [
        {
          id: 1,
          title: "Movimiento",
          description: "Deposito de salario",
          amount: "1000",
        },
        {
          id: 2,
          title: "Movimiento 1",
          description: "Deposito de honorarios",
          amount: "500",
        },
        {
          id: 3,
          title: "Movimiento 3",
          description: "Comida",
          amount: "-100",
        },
        {
          id: 4,
          title: "Movimiento 4",
          description: "Colegiatura",
          amount: "1000",
        },
        {
          id: 5,
          title: "Movimiento 5",
          description: "Reparación equipo",
          amount: "1000",
        },
      ],
    };
  },
};
</script>
