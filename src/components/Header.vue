<template>
    <header>
        <h1>{{title}}</h1>
        <Button text="Add task" color="green" />
        <!-- <Button text="update task" color="blue" />
        <Button text="delete task" color="red" /> -->
    </header>
</template>

<script>
import Button from './Button'

export default {
    name: 'Header',
    props: {
        title: String,
    },
    components:{
        Button
    }
}
</script>



<style scope>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px ;
    }
</style>