<template >
  <td>
    <img class="icon" v-if="elem.icon" v-bind:src="elem.icon"> {{ elem.title }}
  </td>
</template>

<script>
export default {
  props: {
    elem: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>
td {
  padding: 5px;
  border: 1px solid #2c2d31;
}

td:first-child {
  border-left: 0px solid;
}

td:last-child {
  border-right: 0px solid;
}

.icon {
  vertical-align: text-bottom;
  width: 1.5em;
  height: auto;
}
</style>
