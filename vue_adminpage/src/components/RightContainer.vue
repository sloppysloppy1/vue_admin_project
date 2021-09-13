<template>
  <div class="right-container">
    <div class="content">
      Cписки данных
      <h1> Управление пользователями </h1>
      <br>
      <div class="table-name">
        <h3> Список пользователей </h3>
        <input name="search" placeholder="Поиск.."></input>
      </div>
      <table name="table">
        <tr>
          <TabCellName
            v-for="elem in table_names"
            v-bind:elem="elem"
            v-bind:key="elem.id"
          />
        </tr>
        <TabRow
          v-for="elem in examples"
          v-bind:elem="elem"
          v-bind:key="elem.id"
        />
      </table>
      <button name="button" class="add-user-button">Добавить пользователя</button>
    </div>
</div>
</template>

<script>
import TabCellName from "@/components/TabCellName"
import TabRow from "@/components/TabRow"
export default {
  props: ['headers', 'table_names', 'examples'],
  components: {
    TabCellName, TabRow
  }
}
</script>

<style>
h1 {
  font-size: 24px;
  line-height: 45px;
  color: #bcbdc2;
}

h3 {
  font-weight: bold;
}

input {
  height: 25px;
  width: 150px;
  border-radius: 20px;
  border: 1px solid #2c2d31;
  font-family: inherit;
  font-size: inherit;
  color: inherit;
  background: url("../assets/icons/search.svg") no-repeat left #101216;
  background-position-x: left 10px;
  background-size: 1.5em;
  padding: 3px 40px ;
}

.add-user-button {
  text-align: center;
  width: 200px;
  height: 40px;
  border-radius: 20px;
  background: #3381ed;
  color: white;
  border: none;
  font-family: inherit;
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(51,129,237,0.38);
}

table {
  width: 100%;
  border-collapse: collapse;
  margin: 5px 0 20px 0;
}

tr:first-child > td {
    color: #575c62;
}

.right-container {
  flex-grow: 1;
}

.content {
  margin: 35px 40px;
}

.table-name {
  display: flex;
}

.table-name > h3 {
  flex-grow: 1;
}

td {
  padding: 9px;
  border: 1px solid #2c2d31;
}

td:first-child {
  border-left: 0px solid;
}

td:last-child {
  border-right: 0px solid;
}
</style>
