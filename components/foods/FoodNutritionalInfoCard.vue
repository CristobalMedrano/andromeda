<template>
  <div class="grid grid-flow-row shadow-sm rounded-2xl p-2 border bg-white">
    <div class="mt-2 text-center text-base font-medium text-main-dark">
      Información nutricional
    </div>
    <hr class="my-2 mx-2" />
    <div
      v-for="(nutrient, index) in nutritionalInfo"
      :key="index"
      class="grid grid-cols-2 gap-3 px-3 mb-1 h-fit"
    >
      <div class="grid grid-flow-row">
        <div class="text-right text-base">{{ nutrient.name }}:</div>
      </div>
      <div>
        <div class="text-left text-base font-medium text-main-dark">
          {{ nutrient.quantity }} {{ nutrient.unit.toUpperCase() }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    nutritionalInfo: {
      type: Array,
      default: () => [
        { name: "Calorias", quantity: 0, unit: "kcal" },
        { name: "Proteinas", quantity: 0, unit: "gr" },
        { name: "Grasas", quantity: 0, unit: "grs" },
        { name: "Grasas saturadas", quantity: 0, unit: "grs" },
        { name: "Carbohidratos", quantity: 0, unit: "grs" },
        { name: "Fibra", quantity: 0, unit: "grs" },
        { name: "Colesterol", quantity: 0, unit: "mg" },
        { name: "Sodio", quantity: 0, unit: "mg" },
      ],
    },
  },
};
</script>
