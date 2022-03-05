<template>
  <div
    class="-mb-10 h-36 rounded-b-2xl grid grid-flow-row grid-rows-5"
    :class="getDayColor"
  >
    <div class="text-center font-semibold text-lg grid content-end -mb-2">
      Menu {{ getWeekDay }}
    </div>
    <div class="text-center font-bold text-xl grid row-span-2 content-center">
      {{ getFormatedDate }}
    </div>
    <div class="text-center font-semibold text-lg grid content-start -mt-2">
      {{ getFormatedYear }}
    </div>
  </div>
</template>

<script>
export default {
  props: {
    date: {
      type: Date,
      default: () => new Date(),
    },
  },
  computed: {
    getWeekDay() {
      return this.date.getDay() === new Date().getDay() ? "de hoy" : "del día";
    },
    getDayColor() {
      const weekDay = this.date.getDay();
      switch (weekDay) {
        case 1:
          return "bg-fruit-1 text-main-dark";
        case 2:
          return "bg-fruit-2 text-main-dark";
        case 3:
          return "bg-fruit-3 text-main-dark";
        case 4:
          return "bg-fruit-4 text-main-dark";
        case 5:
          return "bg-fruit-5 text-main-dark";
        default:
          return "bg-main-orange";
      }
    },
    getFormatedDate() {
      const days = [
        "Domingo",
        "Lunes",
        "Martes",
        "Miércoles",
        "Jueves",
        "Viernes",
        "Sábado",
      ];
      const months = [
        "Enero",
        "Febrero",
        "Marzo",
        "Abril",
        "Mayo",
        "Junio",
        "Julio",
        "Agosto",
        "Septiembre",
        "Octubre",
        "Noviembre",
        "Diciembre",
      ];
      const weekDay = days[this.date.getDay()];
      const day =
        this.date.getDate() < 10
          ? `0${this.date.getDate()}`
          : this.date.getDate();
      const month = months[this.date.getMonth()];
      return `${weekDay} ${day} de ${month}`;
    },
    getFormatedYear() {
      const year = this.date.getFullYear();
      return `${year}`;
    },
  },
};
</script>
