<template>
    <div>
        <ul v-for="(tarea, index) in listTasks" :key='index'>
            <li>{{tarea}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'TareasPendiente',
    props: {
        listTasks: String
    }
}
</script>

<style>

</style>