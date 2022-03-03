<template>
  <div class="bg-main-blue grid grid-cols-5 px-4 h-10">
    <div class="grid col-span-1 content-center justify-start">
      <AppButtonIcon :svg="svg" />
    </div>
    <div
      class="grid col-span-3 content-center text-white text-base text-center"
    >
      Casino central
    </div>
    <div class="grid col-span-1 content-center justify-end text-white">
      Info
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    svg: "M11,9H9V2H7V9H5V2H3V9C3,11.12 4.66,12.84 6.75,12.97V22H9.25V12.97C11.34,12.84 13,11.12 13,9V2H11V9M16,6V14H18.5V22H21V2C18.24,2 16,4.24 16,6Z",
  }),
};
</script>
