<template>
  <v-app>
    <Header />
    <div class="wrapper">
    <AddTodo @create-card="createCard"/>
    <TodoList v-bind:todo="todocard"
    @delete-todo="deleteTodo"
    />
    </div>
  </v-app>
</template>

<script>
import Header from '@/components/Header'
import AddTodo from '@/components/AddTodo'
import TodoList from '@/components/TodoList'

export default {
  name: 'App',
  data: () => ({
    todocard: []
  }),
  components: {
    Header,
    AddTodo,
    TodoList
  },
  methods: {
    createCard(todo) {
      this.todocard.push(todo);
      console.log(this.todocard)
    },
    deleteTodo(id) {
      this.todocard = this.todocard.filter(todo => todo.id !== id)
    }
  }
};
</script>

<style>
  .wrapper {
    display: flex;
  }
</style>