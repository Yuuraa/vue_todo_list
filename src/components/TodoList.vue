<template>
<div class="todolist">
    <h2>Todo List</h2>
  <!-- <div id="simplebutton"> -->
      <input type="text" class="createTodo" v-model="text" v-on:keyup.enter="createTodo(text)" placeholder="Add new todo">
      <button class="btn add-btn" @click="createTodo(text)">Add</button>
    <!-- <p>{{message}}</p>
    <button v-on:click="reverseMessage">Button</button> -->
    <ol>
        <li class="todo" v-for="(todo, id) in todos">
            {{todo.text}}
                  <button class="btn delete-btn" @click="deleteTodo(id)">Delete</button>

        </li>
    </ol>
</div>
</template>

<script>
export default {
  name: 'TodoList',
  data: () => ({
    todos: [
    ]
  }),
  methods: {
    createTodo: function(text){
        if (text != null){
            this.todos.push({text: text});
            this.text = null;
        }
    },
    deleteTodo: function(id){
        this.todos.splice(id, 1);
    }
  }
}
</script>

<style>
/* #simplebutton {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
} */
</style>
