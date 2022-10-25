<template>
    <header>
        <h1>{{ title }}</h1>
        <my-button @toggle-add-task="$emit('toggle-add-task')" :text="showAddedTask ? 'Close' : 'Add Task'" :color="showAddedTask ? 'crimson' : 'green'"/>
    </header>
</template>

<script>
import MyButton from './MyButton';

    export default {
        name: "my-header",
        props: {
            title: String,
            showAddedTask: Boolean
        },
        components: {
            MyButton
        },
    }
</script>

<style>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>