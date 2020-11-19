<template>
    <div class="list-wrapper">
        <ul>
            <TodoCard 
                v-for="(cardItem, i) of todo" v-bind:key="i"
                v-bind:card="cardItem"
                v-bind:id="i"
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