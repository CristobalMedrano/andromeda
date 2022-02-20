<template>
  <div class="grid grid-rows-4 gap-4">
    <div class="flex justify-center items-center text-white bg-main-blue">
      <div>
        <div class="text-lg font-semibold flex justify-center">Menú de hoy</div>
        <div class="text-sm font-bold flex justify-center">
          Lunes 06 de Diciembre
        </div>
      </div>
    </div>
    <FoodsFoodDetailsCard
      title="Entrada"
      content="Ensalada de mix de repollo con cilantro"
    />
    <FoodsFoodDetailsCard
      title="Plato de fondo"
      content="Fideos con salsa blanca y primavera"
    />
    <FoodsFoodDetailsCard title="Postre" content="Fruta" />
  </div>
</template>

<script>
export default {
  name: "MainPage",
  layout: "DefaultLayout",
};
</script>
