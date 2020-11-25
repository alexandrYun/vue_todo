<template>
    <li>
        <v-card min-width="700" class="todo-card">
            <div>
            <v-card-text>{{id + 1}}</v-card-text>
            <v-card-title>{{card.title}}</v-card-title>
            <v-card-text>Приоритет: {{card.priority}}</v-card-text>
            <v-card-text>Дедлайн: {{card.date}}</v-card-text>
            </div>
            <div>
            <v-btn
            depressed
            color="error"
            @click="$emit('delete-todo', card.id)"
            >
            Удалить
            </v-btn>
            </div>
        </v-card>
    </li>
</template>

<script>
export default {
    props: {
        card: Object,
        id: Number
    }
}
</script>

<style scoped>
    li {
        list-style-type: none;
        margin-bottom: 10px;
    }
    .todo-card {
        padding-right: 50px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    } 
</style>