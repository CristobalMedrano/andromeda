<template>
  <div class="bg-white shadow-sm rounded-2xl h-fit mx-3">
    <div class="grid grid-rows-4 w-full h-full">
      <div
        class="grid content-center justify-center text-base text-main-orange font-semibold"
      >
        {{ title }}
      </div>
      <div class="grid row-span-3">
        {{ content }}
      </div>
      <!-- <div class="grid grid-cols-5 h-2">
        <div class="flex justify-center items-start"></div>
        <div class="col-span-4 grid grid-rows-2 container h-full">
          <div class="flex justify-center text-lg">
            {{ content }}
          </div>
        </div>
      </div> -->
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: "Título",
    },
    content: {
      type: String,
      default: "Contenido",
    },
  },
};
</script>
