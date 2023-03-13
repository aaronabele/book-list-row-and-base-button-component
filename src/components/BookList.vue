<template>
  <table cellspacing="0">
    <thead>
      <th class="table--secondary general-padding">Name</th>
      <th class="table--secondary general-padding">ISBN</th>
      <th class="table--secondary general-padding">Price</th>
      <th class="table--secondary general-padding">Pages</th>
      <th class="table--secondary general-padding">Interested?</th>
    </thead>
    <tbody>
      <tr v-for="book in books" :key="book.isbn">
        <td class="general-padding">{{ book.name }}</td>
        <td class="table-site-border general-padding">{{ book.isbn }}</td>
        <td class="table-site-border general-padding">{{ book.price }}</td>
        <td class="table-site-border general-padding">{{ book.pages }}</td>
        <td class="table-site-border general-padding">
          <BaseButton btnName="Add to Basket" />
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";

export default {
  name: "BookList",
  components: {
    BaseButton,
  },
  data() {
    return {
      books: [
        {
          id: 1,
          name: "Practical Rust Web Projects",
          isbn: 9781484265888,
          price: "$10.10",
          pages: 110,
        },
        {
          id: 2,
          name: "Using WebPagetest",
          isbn: 9781484265888,
          price: "$11.11",
          pages: 200,
        },
        {
          id: 3,
          name: "Web Scraping with Python",
          isbn: 9781491910290,
          price: "$22.22",
          pages: 510,
        },
        {
          id: 4,
          name: "High Performance Mobile Web",
          isbn: 9781491912553,
          price: "$33.33",
          pages: 1100,
        },
      ],
    };
  },
};
</script>

<style>
table {
  margin-left: auto;
  margin-right: auto;
}

:root {
  --primary: purple;
  --primary-dark: rgb(45, 0, 45);
}

.general-padding {
  padding: 5px 10px;
}

.table--secondary {
  width: auto;
  border-bottom: 2px solid var(--primary);
  background-color: transparent;
  color: black;
}

.table-site-border {
  border-left: 2px solid var(--primary);
}
</style>
