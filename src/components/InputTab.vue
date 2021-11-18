<template>
  <div>
    <name v-model="name" />
    <p>Имя пользователя в корневом компоненте: {{ name }}</p>
  </div>
</template>

<script>
import Name from "./Name.vue";

export default {
  name: "InputTab",
  components: { Name },
  data: () => ({
    name: "Masha",
  }),
};
</script>