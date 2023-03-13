<template>
  <BookListRow msg="All Books" />
</template>

<script>
import BookListRow from "./components/BookListRow.vue";

export default {
  name: "App",
  components: {
    BookListRow,
  },
};
</script>

<style>
.btn {
  border: 3px solid transparent;
  border-radius: 3px;
  padding: 5px;
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
