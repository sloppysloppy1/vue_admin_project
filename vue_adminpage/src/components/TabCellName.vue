<template>
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
.icon {
  vertical-align: text-bottom;
  width: 1.5em;
  height: auto;
}
</style>
