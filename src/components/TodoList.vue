<template>
    <div>
        <b-card header="TodoList" header-tag="header">
            <b-list-group>
                <TodoItem v-for="item in list" :todo="item" :key="item.id"/>
            </b-list-group>
            <template v-slot:footer>
                <b-button class="float-right" variant="primary">Add</b-button>
            </template>
        </b-card>
    </div>
</template>

<script>
import TodoItem from "./TodoItem.vue"
export default {
    name: "ToDoList",
    components: {
        TodoItem,
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