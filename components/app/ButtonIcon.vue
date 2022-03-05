<template>
  <button :disabled="disabled" class="w-7 cursor-default">
    <svg
      :class="isDisabledColor"
      class="hover:text-gray-300 active:text-gray-400 cursor-pointer"
      viewBox="0 0 24 24"
      @click="onClick"
    >
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
      default: "text-white ",
    },
    size: {
      type: String,
      default: "w-5 h-5",
    },
    disabled: {
      type: Boolean,
    },
  },

  computed: {
    isDisabledColor() {
      return this.disabled ? "text-gray-400" : this.color;
    },
  },

  methods: {
    onClick() {
      this.$emit("click");
    },
  },
};
</script>
