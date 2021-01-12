<template>
  <div class="datos">
    <input type="text" v-model="task" placeholder="Ingrese una tarea">
    <button @click="add">+</button>
    <tareas-pendiente :listTasks='listTasks'></tareas-pendiente>
  </div>
</template>

<script>
// @ is an alias to /src

import TareasPendiente from '../components/TareasPendiente.vue';

export default {
  name: "Home",
  components: {  TareasPendiente  },
  data() {
    return {
      task: '',
      listTasks: [],
    }
  },
  methods: {
    add() {
      let tarea = this.task;
      if (tarea.length > 0) {
        this.listTasks.push(tarea)
        console.log(this.listTasks)
        this.task = ''
      }
    },
  }
}
</script>
