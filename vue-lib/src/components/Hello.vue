<template>
  <div class="app">Hello <DsiWorld /></div>
</template>

<script>
import DsiWorld from './World.vue'


export default {
  name: "DsiHello",

  components: {
    DsiWorld
  }
};
</script>

<style>
.app {
  color: red;
}
</style>
