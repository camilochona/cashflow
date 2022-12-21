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
        <template #graphic> <Graphic :amounts="amounts" /> </template>
        <template #action>
          <ActionVue />
        </template>
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
import ActionVue from "./Action.vue";
import Graphic from "./Resume/Graphic.vue";

export default {
  components: {
    LayoutVue,
    HeaderVue,
    Resume,
    Movements,
    ActionVue,
    Graphic,
  },
  data() {
    return {
      amount: null,
      amounts: [100, 200, 500, 200, -400, -600, -300, 0, 300, 500],
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
