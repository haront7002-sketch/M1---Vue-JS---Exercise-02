<script setup>
import Header from './components/headerbar.vue'
import Ticketcard from './components/ticketcard.vue';

</script>

<template>
  <div id="app">
  <div>
    <Header />
    <Ticketcard />
  </div>

  </div>
</template>



<style>
body, html, #app {
  margin: 0;
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  color: #222;
  background: #fff;
}

#app {
  min-height: 100vh;
}
</style>

