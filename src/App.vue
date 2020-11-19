<template>
  <v-app>
    <Header />
    <div class="wrapper">
    <AddTodo @create-card="createCard"/>
    <TodoList v-bind:todo="todocard"/>
    </div>
  </v-app>
</template>

<script>
import Header from '@/components/Header'
import AddTodo from '@/components/AddTodo'
import TodoList from '@/components/TodoList'

export default {
  name: 'App',

  components: {
    Header,
    AddTodo,
    TodoList
  },
  methods: {
    createCard(todo) {
      this.todocard.push(todo);
      console.log(this.todocard)
    }
  },
  data: () => ({
    todocard: []
  }),
};
</script>

<style>
  .wrapper {
    display: flex;
  }
</style>