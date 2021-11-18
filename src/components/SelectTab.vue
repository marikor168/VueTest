<template>
  <div>
    <select v-model="selectedFruit">
      <option disabled value="">Выберите любимый фрукт:</option>
      <option v-for="fruit in fruits" :key="fruit" :value="fruit">
        {{ fruit }}
      </option>
    </select>
    <p>Выбранный фрукт: {{ selectedFruit }}</p>
  </div>
</template>

<script>
export default {
  name: "SelectTab",
  data: () => ({
    fruits: ["яблоко", "банан", "лимон", "груша"],
    selectedFruit: "",
  }),
};
</script>