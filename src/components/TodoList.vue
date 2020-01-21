<template>
    <div>
        <b-card header="TodoList" header-tag="header">
            <b-list-group>
                <TodoItem v-on:complete-todo="completeTodo" v-for="item in list" :todo="item" :key="item.id" v-on:delete-todo="deleteTodo"/>
            </b-list-group>
            <template v-slot:footer>
                <input type="text" v-model="todo" v-on:keyup.enter="addNewTodo()"/>
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
                { id: 1, text: "Clean the gaff", done: true },
                { id: 2, text: "Feed people", done: false },
                { id: 3, text: "Cure world hunger", done: false },
                { id: 4, text: "Get good", done: false },
                { id: 5, text: "Yes", done: false },
                { id: 6, text: "Do groceries", done: false },
                { id: 7, text: "Don't forget to sleep!", done: false }
            ],
            todo: ""
        };
    },
    methods: {
        addNewTodo() {
            // Validate Todo:
            if (!this.todo) {
                alert("Enter Todo");
                return;
            }

            // Get max. ID in list and add 1 to it:
            const newId = Math.max.apply(null, this.list.map(t => t.id)) + 1;

            // Add Todo to list with new ID, text in input field and done: false:
            this.list.push({ id: newId, text: this.todo, done: false });

            // Reset Todo input to empty string:
            this.todo = "";
        },
        completeTodo(todo) {
            const todoIndex = this.list.indexOf(todo);
            this.list[todoIndex].done = true;
        },
        deleteTodo(todo) {
            const todoIndex = this.list.indexOf(todo);
            this.list.splice(todoIndex, 1);
        }
    }
};
</script>

<style>

</style>