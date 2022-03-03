<template>
  <button class="w-6 p-2 hover:rounded-full active:rounded-full">
    <svg :class="color" viewBox="0 0 24 24">
      <path fill="currentColor" :d="svg" />
    </svg>
  </button>
</template>

<script>
export default {
  props: {
    svg: {
      type: String,
      default: "Botón",
    },
    color: {
      type: String,
      default: "text-white",
    },
    size: {
      type: String,
      default: "w-5 h-5",
    },
  },
};
</script>
