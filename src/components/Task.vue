<template>
    <div  :class="[task.reminder ? 'reminder' : '' , 'task']">
        <h3>{{task.text}}
            <i @click="onDelete(task.id)" class="fas fa-times"></i>
        </h3>
        <p>{{task.day}}</p>
    </div>
</template>


<script>
export default {
    name: 'Task',
    props: {
        task: Object
    },
    methods:{
        onDelete(id){
            this.$emit('delete-task', id)
            // console.log(id);
        },
    },
}
</script>

<style>
.fas{
    float: right;
    color: red;
    padding: 15px;
}
.task{
    background-color: rgb(231, 231, 231);
    margin: 4px;
    padding: 2px;
    padding-left : 15px;
}
.task.reminder {
    border-left: 8px solid green;
}
</style>