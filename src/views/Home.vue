<template>
  <div class="home">
    <ol>
      <li class="flex" v-for="(a, i) in all" :key="i">
        <p>{{i}}) {{a.id}} - {{a.title}} - {{a.dates}} </p>
        <router-link :to="{name:'about'}"><button @click="editBtn(i)">Edit</button></router-link>
        <button @click="removeBtn(i)">Delete</button>
      </li>
    </ol>
  </div>
</template>

<script>
// @ is an alias to /src

import all from '../all'
export default {
  name: 'home',
  data() {
    return {
      all: [
        { title :  '' },
        { textt : '' },
      ],
    }
  },
  mounted () {
    this.all = all.all
    all.all.id = this.id
  },
  methods: {
    name() {
      this.all = all.all
    },
    editBtn(id) {
      all.all.qw = true
      all.all.id = id
      console.log(all.all.qw)
      console.log(all.id)
    },
    removeBtn(id){
      return all.all.splice(id, 1)
    }
  },
  components: {
    // notes,
  }
  
}
</script>

<style scope>
  .flex{
      width: 50%;
      margin: 0 auto;
      display: flex;
      justify-content: space-around;
  }
</style>

