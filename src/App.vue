<template>
  <div id="app">
    <div>
      <button v-for="tab in tabs" :key="tab" @click="currentTab = tab">
        {{ tab }}
      </button>
    </div>
    <component class="tab-content" :is="currentTab" />

    <card>
      <template #title>Карточка товара</template>
      <template #default="{ product }">
        <p>{{ product.name }}</p>
        <p>{{ product.size }}</p>
      </template>
    </card>
  </div>
</template>

<script>
import InputTab from "./components/InputTab.vue";
import SelectTab from "./components/SelectTab.vue";
import CheckboxTab from "./components/CheckboxTab.vue";
import ComponentTab from "./components/ComponentTab.vue";
import RadioTab from "./components/RadioTab.vue";
import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    InputTab,
    SelectTab,
    CheckboxTab,
    ComponentTab,
    RadioTab,
    Card,
  },
  data: () => ({
    tabs: ["InputTab", "RadioTab", "CheckboxTab", "SelectTab", "ComponentTab"],
    currentTab: "InputTab",
  }),
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.tab-content {
  padding: 20px;
}
</style>
