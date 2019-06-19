<template>
  <div>
    <h1>Notes</h1>
    <label>Title</label><br>
    <input type="text" v-model="title" v-text="all.text"><br>
    <label>Title</label><br>
    <textarea cols="30" rows="10" v-model="textt"></textarea><br>
    <label>Title: </label>
    <input type="date" v-model="dates"><br><br>
    <router-link :to="{name:'home'}"><button @click="clc">Отправить</button></router-link>
  </div>
</template>

<script>
  import all from '../all'
  export default {
    data() {
      return {
        title: '',
        textt: '',
        dates: '2019-06-12',
        all: [],
      }
    },
    methods: {
      clc() {
        this.all = {
          title: this.title,
          textt: this.textt,
          dates: this.dates,
        }
        all.all.push(this.all)
      }
    },
    mounted() {
      this.all = all.all
      if(this.all.qw === true){
        let id = all.all.id
        this.title = all.all[id].title
        this.textt = all.all[id].textt
      }
      if(this.all.qw === false){
        this.title = ''
        this.textt = ''
      }
    },
  }
</script>

<style scoped>

</style>