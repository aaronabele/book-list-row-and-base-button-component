<template>
  <button
    class="btn btn--primary btn--primary:hover"
    @click="$emit('btn-click')"
  >
    <slot name="btn-slot"> </slot>
  </button>
</template>

<script>
export default {
  props: {
    text: String,
    variant: {
      default: "bg--primary",
      validator: (value) => ["bg--primary", "bg--secondary"].includes(value),
    },
  },
  emits: ["btn-click"],
};
</script>

<style>
.btn {
  border: 3px solid transparent;
  border-radius: 3px;
  padding: 5px;
  margin-top: 10px;
  cursor: pointer;
}

.btn--primary {
  border-color: var(--primary-dark);
  background-color: var(--primary);
  color: #fff;
}

.btn--primary:hover {
  border-color: var(--primary);
  background-color: var(--primary-dark);
}

.btn--secondary {
  border-color: var(--primary);
  background-color: transparent;
  color: var(--primary);
}

.btn--secondary:hover {
  background-color: var(--primary);
  color: #fff;
}
</style>
