<template>
    <div>
      <input type="text" v-model="task" placeholder="Agregar una tarea">
      <button @click="agregar">+</button>
      <ul v-for="(tarea, index) in listTasks" :key='index'>
        <h2>Tareas Pendientes</h2>
        <input type="checkbox" name="" id=""><li>{{tarea}}</li>
      </ul>
    </div>
</template>

<script>
// @ is an alias to /src
import TareasPendiente from '../components/TareasPendiente'

export default {
  name: "Home",
  component: {  TareasPendiente  },
  data() {
    return {
      task: '',
      listTasks: []
    }
  },
  methods: {
    agregar() {
      let tasks = this.task
      this.listTasks.push(tasks)
      console.log(this.listTasks)
    }
  },
  // computed: {
  //   agregar() {
  //     let tasks = [];
  //     tasks.push(this.task)
  //     console.log(tasks)
  //   }
  // }
};
</script>
