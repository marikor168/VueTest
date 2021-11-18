<template>
  <div>
    <p>Вы готовы к переезду?</p>

    <input type="radio" id="yes" value="Да" v-model="picked" />
    <label for="yes">Да</label>

    <input type="radio" id="no" value="Нет" v-model="picked" />
    <label for="no">Нет</label>

    <p>Ответ: {{ picked }}</p>
  </div>
</template>

<script>
export default {
  name: "RadioTab",
  data: function () {
    return {
      picked: "",
    };
  },
};
</script>