<template>
  <tr>
    <td>
      {{ elem.id }}
    </td>
    <td>
      {{ elem.name }}
    </td>
    <td>
      {{ elem.email }}
    </td>
    <td>
       <p v-if="elem.status=='active'"> &#9989; Активен</p>
       <p v-else="elem.status=='not-active'"> &#10060; Неактивен</p>
    </td>
    <td>
      <center>
        <v-select :items="['Canada', 'United States']"></v-select>
      </center>
    </td>
  </tr>
</template>

<script>
export default {
  props: {
    elem: {
      type: Object,
      required: true
    }
  },

  data() {
    return {
      actions_dropdown: [
        {id: 0, title: "Удалить пользователя"},
        {id: 1, title: "Редактировать"},
        {id: 2, title: "Забанить"},
      ]
    }
  }
}
</script>

<style scoped>
td {
  padding-left: 12px;
}
</style>
