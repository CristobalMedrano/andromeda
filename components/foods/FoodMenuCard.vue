<template>
  <div
    class="shadow-sm rounded-2xl px-2 py-1 border bg-white grid grid-cols-4 h-fit"
  >
    <div class="grid col-span-1 content-center justify-center">
      <svg class="w-10 h-10 text-main-dark" viewBox="0 0 24 24">
        <path fill="currentColor" :d="svg" />
      </svg>
    </div>
    <div class="grid col-span-3 my-2">
      <div class="text-left text-base font-medium text-main-dark">
        {{ title }}:
      </div>
      <div class="text-left text-lg font-normal pr-2 text-main-dark">
        {{ content }}
      </div>
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
    svg: {
      type: String,
      default:
        "M11,9H9V2H7V9H5V2H3V9C3,11.12 4.66,12.84 6.75,12.97V22H9.25V12.97C11.34,12.84 13,11.12 13,9V2H11V9M16,6V14H18.5V22H21V2C18.24,2 16,4.24 16,6Z",
    },
  },
};
</script>
