<template>
  <div :class="$style.box">
    <!-- 
     -->

    <h2 :class="$style.text">Информация о книгах</h2>
    <BooksItem 
        v-for="book in books" 
        :key="book.id" 
        :book="book" />

    <!-- 
      -->
  </div>
</template>

<script>
import BooksItem from "@/components/Task3Child.vue";

export default {
  name: "Task3Sem2",

  components: {
    BooksItem,
  },

  data() {
    return {
      books: [
        { id: 1, title: "Книга 1", author: "Автор 1", year: 2020 },
        { id: 2, title: "Книга 2", author: "Автор 2", year: 2019 },
        { id: 3, title: "Книга 3", author: "Автор 3", year: 2021 },
      ],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" module>
.box {
  margin-bottom: 150px;
}
.text {
  color: blue;
}
</style>

<!-- Разработка приложения для отображения информации о книгах
Требуется создать компонент "Книга" (Book), который будет отображать информацию о книге, такую как название, автор и год издания. Компонент "Книга" должен иметь возможность отображать дополнительные детали о книге по требованию пользователя. Также необходимо создать компонент "Список книг" (BookList), который будет отображать список книг из переданного массива. -->
