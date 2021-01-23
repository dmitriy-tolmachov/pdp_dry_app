<template>
  <div id="app">
    <h1>GGGGGGGG</h1>
    <hr>
    <TodoList/>
  </div>
</template>

<script>

import TodoList from '@/components/TodoList'

export default {
  name: 'App',
  components: {
    TodoList
  },
  methods: {
    fetchUsers: function () {
      const baseURI = 'https://jsonplaceholder.typicode.com/users'
      this.$http.get(baseURI)
              .then((result) => {
                this.users = result.data
              })
    }
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

