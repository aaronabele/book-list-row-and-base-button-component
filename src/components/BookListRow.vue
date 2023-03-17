<template>
  <tr class="table-item__table">
    <td>{{ title }}</td>
    <td>{{ isbn }}</td>
    <slot name="actionCol"> </slot>
  </tr>
</template>

<script>
export default {
  props: {
    title: String,
    isbn: String,
  },
};
</script>

<style>
.table-item__table td {
  padding: 20px 15px;
}
</style>
