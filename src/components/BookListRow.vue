<template>
  <h1 class="main-header-styling">{{ msg }}</h1>
  <BookList />
</template>

<script>
import BookList from "./BookList.vue";

export default {
  name: "BookListRow",
  components: {
    BookList,
  },
  props: {
    msg: String,
  },
};
</script>

<style>
.main-header-styling {
  width: 100%;
  text-align: center;
  font-size: 38px;
  text-decoration: underline purple;
}
</style>
