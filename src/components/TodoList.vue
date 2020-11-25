<template>
    <div class="list-wrapper">
        <ul>
            <TodoCard 
                v-for="(cardItem, i) of todo" v-bind:key="i"
                v-bind:card="cardItem"
                v-bind:id="i"
                @delete-todo="deleteTodo"
            />
        </ul>
    </div>    
</template>

<script>
import TodoCard from '@/components/TodoCard'
export default {
    props: ['todo'],
    components: {
        TodoCard
    },
    methods: {
        deleteTodo(id) {
            this.$emit('delete-todo', id)
        }
    }
}
</script>

<style scoped>
    .list-wrapper {
        margin: 10px 10px 10px 320px;
        width: 100%;
    }

    ul {
        padding: 0;
    }
</style>