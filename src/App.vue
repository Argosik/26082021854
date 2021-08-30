<template>
<div id="app">
<AdPost />
<AddComment 
    @add-todo="addTodo"
/>
<CommentList
  v-bind:Comms="Comms"
/>
</div>
</template>

<script>
import CommentList from '@/components/CommentList'
import AddComment from '@/components/AddComment'
import AdPost from '@/components/AdPost'
export default {
  name: 'App',
  data() {
    return {
      Comms: [
        {id: 1, title: 'Тестовый коммент'},
      ]
    }
  },

  methods: {
addTodo(todo) {
  this.Comms.push(todo)
}


  },
  components: {
    CommentList, AddComment, AdPost
  
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

