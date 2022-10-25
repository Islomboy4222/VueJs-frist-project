<template>
    <div v-for="task in tasks" :key="task.id">
        <my-task @toggle-reminder="$emit('toggle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" :task="task"/>
    </div>
</template>

<script>
import MyTask from './MyTask'
    export default {
        name: "my-tasks",
        components: {
            MyTask
        },
        props: {
            tasks: Array
        },
        emits: ['delete-task', 'toggle-reminder']
    }
</script>