<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Все записи</router-link> |
      <router-link to="/about"><button @click="qwqw">Добавить запись</button></router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
  import all from './all'
  export default {
    methods: {
      qwqw() {
        all.all.qw = false
        console.log(all.all.qw)
      }
    },
  }
</script>

<style>

</style>
