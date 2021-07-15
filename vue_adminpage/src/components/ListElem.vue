<template>
  <li tabindex="1">
   {{elem.title}}
  </li>
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
  li {
    list-style-type: none;
  }

  li:focus {
    background-color: #23252a;
  }
</style>
