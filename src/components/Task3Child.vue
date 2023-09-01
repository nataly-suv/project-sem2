<template>
  <div>
    <!--         
     -->
    <h3 @click="toggle">Название книги: {{ book.title }}</h3>
    <div v-if="showDescription">
      <p>Автор: book.author</p>
      <p>Год издания: book.year</p>
    </div>
    <!--         
     -->
  </div>
</template>

<script>
export default {
  name: "BooksItem",
  props: ["book"],

  data() {
    return {
      showDescription: false,
    };
  },

  mounted() {},

  methods: {
    toggle() {
      this.showDescription = !this.showDescription;
    },
  },
};
</script>

<style lang="scss" scoped></style>
