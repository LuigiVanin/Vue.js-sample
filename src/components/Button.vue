<template>
    <button @click="onClick()" class="btn" :style="{ background: color }">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: "Button",
    props: {
        text: {
            type: String,
            default: "add",
        },
        color: {
            type: String,
            default: "red",
        },
    },
    methods: {
        onClick() {
            this.$emit("toggle");
        },
    },
};
</script>

<style scoped>
button {
    transition: 0.5s;
    text-align: center;
    font-weight: bold;
    width: 150px;
}
</style>
