<template>
  <div id="app">
    <task-list name="Todo List">
      <task-item v-for="(item,index) in todos" :key="index">{{item}}</task-item>
      <task-item>
        <input id="newone" type="text" v-model="newtodo" @keyup.enter="addTodo" placeholder="Add New">
      </task-item>
    </task-list>
  </div>
</template>

<script>
import TaskList from './components/TaskList.vue'
import TaskItem from './components/TaskItem.vue'

export default {
  name: 'app',
  components: {
    TaskList,
    TaskItem
  },
  data:()=> {
    return {
      todos: [
        "Do Laundry",
        "Bath",
        "Buy Food",
        "Sleep",
      ],
      newtodo: "",
    }
  },
  methods : {
    addTodo() {
      this.todos.push(this.newtodo);
      this.newtodo = "";
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#newone {
  width: 100%;
  height: 100%;
  border: 0;
  font-size: 20px;
  text-align: center;
}
#newone:focus {
  outline:0;
  border: 0;
}
</style>
