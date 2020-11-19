<template>
    <li>
        <v-card min-width="700">
            <v-card-text>{{this.id + 1}}</v-card-text>
            <v-card-title>{{card.title}}</v-card-title>
            <v-card-text>{{card.priority}}</v-card-text>
            <v-card-text>Дедлайн: {{card.date}}</v-card-text>
        </v-card>
    </li>
</template>

<script>
export default {
    props: {
        card: {
            type: Object
        },
        id: Number
    }
}
</script>

<style scoped>
    li {
        list-style-type: none;
        margin-bottom: 10px;
    }    
</style>