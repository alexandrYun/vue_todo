<template>
  <div class="addtodo-wrapper">
    <v-text-field
        regular
        label="Дело"
        clearable
        class="todo__title"
        v-model="todo_title"
        >
    </v-text-field>
      <v-select
        :items="items"
        label="Приоритет"
        dense
        solo
        class="todo__priopity"
        v-model="priority"
      ></v-select>
    <span>Дедлайн:</span>
    <v-date-picker
        v-model="date"
        full-width
        class="todo__deadline"
      ></v-date-picker>
    <v-btn
      class="mx-2"
      fab
      dark
      color="indigo"
      @click="addTodo"
    >
      <v-icon dark>
        mdi-plus
      </v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
    date: new Date().toISOString().substr(0, 10),
    items: ['High', 'Medium', 'Low'],
    todo_title: '',
    priority: ''
    }
  },
  methods: {
    addTodo() {
      const newTodo = {
        title: this.todo_title,
        priority: this.priority,
        date: this.date
      }
      this.$emit('create-card', newTodo)
    }
  }
}
</script>

<style>
  .addtodo-wrapper {
    width: 300px;
    display: flex;
    flex-direction: column;
    align-items: center;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    border-radius: 10px;
    margin: 10px 10px;
    padding: 10px;
    max-height: 584px;
    position: fixed;
  }
  .todo__title, .todo__priopity {
    width: 250px;
  }
  .todo__deadline {
    height: 350px;
  }
</style>