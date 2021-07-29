<template>
  <div id="app">
    <banner></banner>
    <first></first>
  </div>
</template>

<script>

import first from "./components/first.vue";
import banner from "./components/banner.vue";

export default {
  name: 'App',
  components: {
      'first': first,
      'banner': banner,
  }
}

</script>

<style>
</style>
