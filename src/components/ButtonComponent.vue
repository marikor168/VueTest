<template>
  <div>
    <button @click="$emit('change-msg', 'Пока')">
      <slot />
    </button>
  </div>
</template>

<script>
export default {
  name: "ButtonComponent",
};
</script>