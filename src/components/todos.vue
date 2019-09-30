<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in Todos"> 
            <todoitem v-bind:todo="todo" v-on:del-todo="$emit('del-todo', todo.id)"/>
        </div>

    </div>
</template>

<script>
import todoitem from './todoitem.vue';

export default {
    name: "todos",
    components : {
        todoitem
    },
    props: ["Todos"]   
} 
</script>

<style scoped>
 
</style>