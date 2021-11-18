<template>
  <div class="card">
    <slot name="title">
      <h4>Заголовок карточки</h4>
    </slot>
    <slot name="subtitle">
      <h6>Подзаголовок карточки</h6>
    </slot>
    <slot :product="product">
      <p>Товар: {{ product.name }}</p>
      <p>Размер: {{ product.size }}</p>
      <p>Описание: {{ product.description }}</p>
    </slot>
    <slot name="actions">
      <div class="btns">
        <button class="btn btn_red">Отмена</button>
        <button class="btn btn_green">Купить</button>
      </div>
    </slot>
  </div>
</template>

<script>
export default {
  name: "Card",
  data: () => ({
    product: {
      name: "Кроссовки",
      size: 37,
      description: "Удобные, на каждый день",
    },
  }),
};
</script>

<style scoped>
.card {
  padding: 20px;
  border: 1px solid goldenrod;
  border-radius: 5px;
}

.btns {
  display: flex;
  column-gap: 20px;
}

.btn {
  padding: 5px 10px;
  border: 1px solid;
  border-radius: 5px;
  color: white;
}

.btn:hover {
  cursor: pointer;
}

.btn_green {
  border-color: green;
  background-color: green;
}

.btn_red {
  border-color: red;
  background-color: red;
}
</style>