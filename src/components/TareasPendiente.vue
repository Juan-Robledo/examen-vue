<template>
    <div class="pendientes">
        <h3>Tareas Pendientes</h3>
        <ul v-for="(tasks, index) in listTasks" :key='index'>
            <li>{{tasks}}
                <input type="checkbox" :name="tasks" v-model="checked" @click="stateTasks">
            </li>
        </ul>
    </div>
        <div class="listas">
        <h3>Tareas Listas</h3>
        <ul v-for="(ctasks, index) in completeTasks" :key='index'>
            <li>{{ctasks}}
                <input type="checkbox" v-model="checked" @click="stateTasks">
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'TareasPendiente',
    props: {
        listTasks: String
    },
    data() {
        return {
            checked: false,
            completeTasks: []
        }
    },
    methods: {
        stateTasks() {
            let state = this.checked;
            if (state != false) {
                this.completeTasks.push(state.tasks)
            }
            console.log(state)
        }
    },
}
</script>

<style>

</style>