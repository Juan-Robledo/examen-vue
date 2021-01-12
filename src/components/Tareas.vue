<template>
    <div v-for="(tarea, index) in tareas" :key='index'>
        <input type="checkbox" name="tarea" id="">
        <span>{{tarea}}</span>
    </div>
</template>

<script>
export default {
    name: 'Tareas',
    props: {
        tareas: String
    }
}
</script>

<style>

</style>