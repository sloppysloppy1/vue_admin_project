<template>
  <div class="left-container">
    <div class="logo">
      logo
    </div>
    <div class="menu">
      <h2>{{ headers[0].title }}</h2>
      <ul>
        <ListElem
          v-for="(item, index) in 2"
          v-bind:elem="stats[index]"
        />
        </br>
        <ListElem
          v-bind:elem="stats[2]"
        />
      </ul>
      </br>
      <h2>{{ headers[1].title }}</h2>
      <ListElem
        v-for="elem in user_tasks"
        v-bind:elem="elem"
      />
    </div>
    <div class="library">
      asdasdas
    </div>
  </div>
</template>

<script>
import ListElem from "@/components/ListElem"
export default {
  props: ['stats', 'headers', 'user_tasks'],
  components: {
    ListElem
  }
}
</script>

<style>

h2 {
  font-size: 18px;
  line-height: 45px;
  color: #4d5258;
}

.left-container {
  width: 22%;
  border-right: 1px solid #2c2d31;
  display: flex;
  flex-direction: column;
}

.logo {
  margin: 0 0;
  border-bottom: 1px solid #2c2d31;
  min-height: 50px;
}

.menu {
  margin: 25px 20px;
}

.library {
  margin: 0 20px;
  align-self: flex-end;
}

</style>
