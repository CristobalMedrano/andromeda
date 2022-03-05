<template>
  <div class="bg-gray-700 grid grid-cols-5 px-3 h-10 sticky top-0">
    <div class="grid col-span-1 content-center justify-start">
      <!-- <AppButtonIcon :svg="homeIcon" disabled />-->
    </div>
    <div
      class="grid col-span-3 content-center text-white text-base text-center"
    >
      Minuta - Casino central
    </div>
    <div class="grid col-span-1 content-center justify-end">
      <AppButtonIcon :svg="infoIcon" @click="onClickInfo" />
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    homeIcon:
      "M10.55 2.533a2.25 2.25 0 0 1 2.9 0l6.75 5.695c.508.427.8 1.056.8 1.72v9.802a1.75 1.75 0 0 1-1.75 1.75h-3a1.75 1.75 0 0 1-1.75-1.75v-5a.75.75 0 0 0-.75-.75h-3.5a.75.75 0 0 0-.75.75v5a1.75 1.75 0 0 1-1.75 1.75h-3A1.75 1.75 0 0 1 3 19.75V9.947c0-.663.292-1.292.8-1.72l6.75-5.694Z",
    leftArrowIcon:
      "M10.295 19.716a1 1 0 0 0 1.404-1.425l-5.37-5.29h13.67a1 1 0 1 0 0-2H6.336L11.7 5.714a1 1 0 0 0-1.404-1.424l-6.924 6.822a1.25 1.25 0 0 0 0 1.78l6.924 6.823Z",
    infoIcon:
      "M12 1.999c5.524 0 10.002 4.478 10.002 10.002 0 5.523-4.478 10.001-10.002 10.001-5.524 0-10.002-4.478-10.002-10.001C1.998 6.477 6.476 1.999 12 1.999Zm-.004 8.25a1 1 0 0 0-.992.885l-.007.116.003 5.502.007.117a1 1 0 0 0 1.987-.002L13 16.75l-.003-5.501-.007-.117a1 1 0 0 0-.994-.882ZM12 6.5a1.251 1.251 0 1 0 0 2.503A1.251 1.251 0 0 0 12 6.5Z",
  }),
  methods: {
    onClickInfo() {
      console.log("Info Button");
    },
  },
};
</script>
