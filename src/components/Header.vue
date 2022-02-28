<template>
    <header>
        <h1>{{ tittle }}</h1>
        <Button
            @toggle="$emit('toggle')"
            :color="showAddTask ? 'red' : 'green'"
            :text="showAddTask ? 'Close' : 'Add Task'"
        />
    </header>
</template>

<script>
import Button from "./Button.vue";
export default {
    name: "Header",
    props: {
        tittle: {
            type: String,
            default: "Task Tracker",
        },
        showAddTask: Boolean,
    },
    components: {
        Button,
    },
};
</script>

<style scoped>
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}
</style>
