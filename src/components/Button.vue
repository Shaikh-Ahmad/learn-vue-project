<template>
    <button class="btn" @click="onClick()" :style="{background : color}">{{text}}</button>
</template>

<script>
export default {
    name: 'Button',
    props:{
        text:String,
        color:String

    },
    methods: {
        onClick(){
            console.log('btn click');
        }
    }
}

</script>

<style>
.btn{
    color : white;
    width: 80px;
    height: 50px;
}
</style>