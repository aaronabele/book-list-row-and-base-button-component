<template>
  <tr class="table-item__table">
    <td>{{ title }}</td>
    <td>{{ isbn }}</td>
    <td>
      <BaseButton variant="bg--primary" @btn-click="handleBookmarkButtonClick">
        <template #btn-slot>
          <svg
            v-if="isBookmarked === true"
            class="symbol"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 30 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M10 18a8 8 0 100-16 8 8 0 000 16zM8.707 7.293a1 1 0 00-1.414 1.414L8.586 10l-1.293 1.293a1 1 0 101.414 1.414L10 11.414l1.293 1.293a1 1 0 001.414-1.414L11.414 10l1.293-1.293a1 1 0 00-1.414-1.414L10 8.586 8.707 7.293z"
              clip-rule="evenodd"
            />
          </svg>
          <svg
            v-else
            class="symbol"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 30 20"
            fill="currentColor"
          >
            <path
              fill-rule="evenodd"
              d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-11a1 1 0 10-2 0v2H7a1 1 0 100 2h2v2a1 1 0 102 0v-2h2a1 1 0 100-2h-2V7z"
              clip-rule="evenodd"
            />
          </svg>

          {{ buttonLabel }}
        </template>
      </BaseButton>
    </td>
  </tr>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";
export default {
  components: {
    BaseButton,
  },
  props: {
    title: String,
    isbn: String,
    isBookmarked: Boolean,
  },
  methods: {
    handleBookmarkButtonClick() {
      this.$emit("bookmark-clicked", this.isbn);
    },
  },
  computed: {
    buttonLabel() {
      return this.isBookmarked ? "Remove Bookmark" : "Add Bookmark";
    },
  },
};
</script>

<style>
.table-item__table td {
  padding: 20px 15px;
}
</style>
