<template>
  <div id="app">
    <div class="box">
      <LeftContainer
        v-bind:stats="stats"
        v-bind:headers="headers"
        v-bind:user_tasks="user_tasks"
      />
      <RightContainer
        v-bind:table_names="table_names"
        v-bind:examples="examples"
      />
      </div>
    </div>
  </div>
</template>

<script>
import LeftContainer from "@/components/LeftContainer"
import RightContainer from "@/components/RightContainer"
import vSelect from "vue-select"
export default {
  name: 'App',
  components: {
    LeftContainer, RightContainer, vSelect
  },

  data() {
    return {
      stats: [
        {id: 0, title: "Публикации"},
        {id: 1, title: "Мессенджер"},
        {id: 2, title: "Подписка на ежедневную рассылку"}
      ],

      headers: [
        {id: 0, title: "Статистика"},
        {id: 1, title: "Списки данных"},
        {id: 2, title: "Cписок пользователей"}
      ],

      user_tasks: [
        {id: 0, title: "Доступные города"},
        {id: 1, title: "Заблокированные пользователи"},
        {id: 2, title: "Черный список ссылок"},
        {id: 3, title: "Управление пользователями"}
      ],

      table_names: [
        {id: 0, title: "ID", icon: require("@/assets/icons/list.svg")},
        {id: 1, title: "Имя", icon: require("@/assets/icons/user.svg")},
        {id: 2, title: "e-mail", icon: require("@/assets/icons/at-sign.svg")},
        {id: 3, title: "Статус", icon: require("@/assets/icons/info.svg")},
        {id: 4, title: "Действия", icon: require("@/assets/icons/disc.svg")}
      ],

      examples: [
        {id: 0, name: "Artur", email: "whoasked@gmail.com", status: "active"},
        {id: 1, name: "Artur", email: "whoasked@gmail.com", status: "not-active"}
      ]
    }
  }
}
</script>

<style>
@import url(http://fonts.googleapis.com/css?family=Roboto:400,100,100italic,300,300ita‌​lic,400italic,500,500italic,700,700italic,900italic,900);
body {
  font-family: 'Roboto', sans-serif;
  line-height: 30px;
  background-color: #101216;
  color: #919299;
}

* {
  margin: 0;
  padding: 0;
}

.box {
  display: flex;
}
</style>
