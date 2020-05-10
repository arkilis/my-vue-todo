<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <AddTodo />
    <ul>
      <li v-for="todo in todos" v-bind:key="todo.id">
        <!-- {{index}} : {{todo}} -->
        <MyTodoView :my-value="{{todo}}" />
      </li>
    </ul>
  </div>
</template>

<script>
import AddTodo from "./components/AddTodo.vue";
import MyTodoView from "./components/Todo.vue";

export default {
  name: "App",
  components: {
    AddTodo,
    MyTodoView
  },
  data() {
    return {
      todos: ["finish vue tutorial", "update linkedin", "send email"]
    };
  }
};
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
AddTodo {
  margin-top: 100px;
  margin-bottom: 100px;
}
</style>
