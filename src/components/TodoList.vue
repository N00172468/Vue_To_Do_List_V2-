<template>
    <div>
        <b-card header="TodoList" header-tag="header">
        <template v-slot:footer>
            <b-button class="float-right" variant="primary">Add</b-button>
        </template>
    </div>
</template>

<script>
export default {
    name: 'ToDoList',
    components: {

    },
    data() {
        return {
            list: [
                { id: 1, text: "Clean thy gaff", done: true },
                { id: 2, text: "Feed thy peasanth", done: false },
                { id: 3, text: "Create thy To Do Appeth", done: false }
            ]
        };
    },
    methods: {

    }
};
</script>

<style>

</style>