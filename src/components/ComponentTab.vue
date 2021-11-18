<template>
  <div>
    <button-component @change-msg="currentMsg = $event">Click</button-component>
    <p>Текущее сообщение: {{ currentMsg }}</p>
  </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";
export default {
  name: "ComponentTab",
  components: { ButtonComponent },
  data: () => ({
    currentMsg: "Привет",
  }),
};
</script>