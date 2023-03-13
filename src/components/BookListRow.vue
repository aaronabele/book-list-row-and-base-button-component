<template>
  <h1>{{ msg }}</h1>
  <table>
    <thead>
      <th class="th.table-item__table-head--action">Name</th>
      <th class="th.table-item__table-head--action">ISBN</th>
      <th class="th.table-item__table-head--action"></th>
    </thead>
    <tbody>
      <tr>
        <td>Practical Rust Web Projects</td>
        <td>9781484265888</td>
        <td><BaseButton btnName="Add Bookmark" /></td>
      </tr>
      <tr>
        <td>Using WebPagetest</td>
        <td>9781484265888</td>
        <td><BaseButton btnName="Add Bookmark" /></td>
      </tr>
      <tr>
        <td>Web Scraping with Python</td>
        <td>9781491910290</td>
        <td><BaseButton btnName="Add Bookmark" /></td>
      </tr>
      <tr>
        <td>High Performance Mobile Web</td>
        <td>9781491912553</td>
        <td><BaseButton btnName="Add Bookmark" /></td>
      </tr>
    </tbody>
  </table>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";

export default {
  name: "BookListRow",
  components: {
    BaseButton,
  },
  props: {
    msg: String,
  },
};
</script>

<style></style>
