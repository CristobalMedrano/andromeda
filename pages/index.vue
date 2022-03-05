<template>
  <div class="grid grid-flow-row gap-3 pb-4 h-fit">
    <FoodsFoodMenuDay :date="api.date" />
    <FoodsFoodMenuList :food-menu="api.menu" class="px-3" />
    <FoodsFoodNutritionalInfoCard
      :nutritional-info="api.nutritionalInfo"
      class="mx-3"
    />
  </div>
</template>

<script>
export default {
  name: "MainPage",
  layout: "DefaultLayout",
  data: () => ({
    api: {
      date: new Date("2022,3,4"),
      menu: [
        {
          title: "Entrada",
          content: "Ensalada de mix de repollo con cilantro",
          svg: "M11,9H9V2H7V9H5V2H3V9C3,11.12 4.66,12.84 6.75,12.97V22H9.25V12.97C11.34,12.84 13,11.12 13,9V2H11V9M16,6V14H18.5V22H21V2C18.24,2 16,4.24 16,6Z",
        },
        {
          title: "Plato de fondo",
          content: "Fideos con salsa blanca y primavera",
          svg: "M12.5,1.5C10.73,1.5 9.17,2.67 8.67,4.37C8.14,4.13 7.58,4 7,4A4,4 0 0,0 3,8C3,9.82 4.24,11.41 6,11.87V19H19V11.87C20.76,11.41 22,9.82 22,8A4,4 0 0,0 18,4C17.42,4 16.86,4.13 16.33,4.37C15.83,2.67 14.27,1.5 12.5,1.5M12,10.5H13V17.5H12V10.5M9,12.5H10V17.5H9V12.5M15,12.5H16V17.5H15V12.5M6,20V21A1,1 0 0,0 7,22H18A1,1 0 0,0 19,21V20H6Z",
        },
        {
          title: "Postre",
          content: "Fruta",
          svg: "M20,10C22,13 17,22 15,22C13,22 13,21 12,21C11,21 11,22 9,22C7,22 2,13 4,10C6,7 9,7 11,8V5C5.38,8.07 4.11,3.78 4.11,3.78C4.11,3.78 6.77,0.19 11,5V3H13V8C15,7 18,7 20,10Z",
        },
      ],
      nutritionalInfo: [
        { name: "Calorias", quantity: 476, unit: "kcal" },
        { name: "Proteinas", quantity: 32, unit: "gr" },
        { name: "Grasas", quantity: 11, unit: "grs" },
        { name: "Grasas Saturadas", quantity: 3, unit: "grs" },
        { name: "Carbohidratos", quantity: 61, unit: "grs" },
        { name: "Fibra", quantity: 7, unit: "grs" },
        { name: "Colesterol", quantity: 1, unit: "mg" },
        { name: "Sodio", quantity: 355, unit: "mg" },
      ],
    },
  }),
};
</script>
