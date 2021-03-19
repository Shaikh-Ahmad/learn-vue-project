<template>
  <div class="container">
    <Header title="Task Traker"/>
  </div>
</template>

<script>
import Header from './components/Header'

export default {
  name: 'App',
  components: {
    Header,
  },
  data(){
    return{
      tasks : [ ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px;
}
.container{
  width: 70%;
  margin: 60px;
  padding: 30px;
  border: 2px solid grey;
}
</style>
