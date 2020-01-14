<template>
    <b-list-group-item>
        {{ todo.text }}    
    </b-list-group-item>    
</template>

<script>
export default {
    name: "TodoItem",
    props: {
        todo: {
            type: Object,
            required: true
        }
    },
};
</script>

<style>

</style>