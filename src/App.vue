<template>
  <div class="container">
    <Header title="Task Traker"/>
    <Tasks @delete-task="deleteTask" :tasks="tasks" />
  </div>
</template>

<script>
import Header from './components/Header'
import Tasks from './components/Tasks.vue'

export default {
  name: 'App',
  components: {
    Header,
    Tasks,
  },
  data(){
    return{
      tasks : [ ]
    }
  },
  methods:{
    deleteTask(id){
      if(confirm('Are you sure you want to delete')){
      // console.log('task' , id)
      this.tasks = this.tasks.filter( (task) => task.id !== id )
      }
    },
  },
  
  created(){
    this.tasks = [
      {
        id: 1,
        text: 'meeting',
        day: '2 feb 2021',
        reminder: true,
      },
      {
        id: 2,
        text: 'doc appoitment',
        day: '2 feb 2021',
        reminder: true,
      },
      {
        id: 3,
        text: 'school meeting',
        day: '20 april 2021',
        reminder: true,
      },
      {
        id: 4,
        text: 'client meeting',
        day: '5 feb 2021',
        reminder: false,
      },
     
    ]
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}
.container{
  
  width: 70%;
  padding: 30px;
  border: 1px solid grey;
}
</style>
