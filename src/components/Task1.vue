<template>
  <!-- 
     -->
  <div :class="$style.box">
    <h2 :class="$style.text">Аутентификация</h2>
    <div v-if="!isAuthenticated">
      <form @submit="login">
        <label for="userName">Имя пользователя</label>
        <input type="text" id="userName" v-model="userName" required />
        <label for="password">Пароль</label>
        <input type="password" id="password" v-model="password" required />
        <button type="submit">Отправить</button>
      </form>
    </div>

    <div v-else>
      <p>Успешная аутентификация! Добро пожаловать!</p>
    </div>
  </div>
  <!-- 
     -->
</template>

<script>
export default {
  name: "Task1Sem2",

  data() {
    return {
      userName: "",
      password: "",
      isAuthenticated: false,
    };
  },

  mounted() {},

  methods: {
    login() {
      this.isAuthenticated = true;
    },
  },
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

<!-- Создайте компонент "Аутентификация" (Authentication), 
    который будет отображать форму входа или сообщение об успешной аутентификации 
    в зависимости от переданного пропса isAuthenticated. 
    Используйте директиву v-if для условного отображения разных элементов в шаблоне компонента. -->
