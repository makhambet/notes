<template>
    <div class="flex">
        <p>
            {{notes.title}} - {{notes.dates}}
        </p>
        <button @click="editBtn()">Edit</button>
        <button @click="removeBtn()">Delete</button>
    </div>
</template>

<script>
    import all from '../all'
    export default {
        props: {
            "notes": {
                type: Object,
                required: true
            },
            "id":{
                type: Number,
                default: 1
            }
        },
        methods: {
            editBtn() {
                return all.splice(notes.id, 1)
            },
            removeBtn(){

            }
        },
    }
</script>

<style scoped>
    .flex{
        width: 50%;
        margin: 0 auto;
        display: flex;
        justify-content: space-around;
    }
</style>