<template>
  <div>
    <p>Выберите свои навыки:</p>
    <div v-for="skill in skills" :key="skill">
      <input
        type="checkbox"
        :id="skill"
        :value="skill"
        v-model="checkedSkills"
      />
      <label :for="skill">{{ skill }}</label>
    </div>

    <p>Ответ: {{ checkedSkills }}</p>
  </div>
</template>

<script>
export default {
  name: "CheckboxTab",
  data: function () {
    return {
      skills: ["vue", "react", "tailwind", "vuetify", "redux", "material-UI"],
      checkedSkills: [],
    };
  },
};
</script>