<template>
    <div :key="tasky.id" v-for="tasky in tasksprop">
        <Task @toggle-reminder="$emit('toggle-reminder', tasky.id)" @delete-task="$emit('delete-task', tasky.id)" :task="tasky" />
    </div>
</template>

<script>
import Task from "./Task.vue"

export default {
    name: "Tasks",
    components: {
        Task,
    },
    props:{
        tasksprop: Array
    },
    emits: ['delete-task', 'toggle-reminder'],
}
</script>



<style scoped>

</style>