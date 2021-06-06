<template>
  <div id="app">

 <TaskList :data-list="DataList"
           @remove-task="removeTask"
           @add-task="addTask"/>         

 
 </div>
</template>
<script>

import TaskList from './components/DZ3/TaskList.vue'
export default {
  name: 'App',
  methods: {
   removeTask(id){
     this.DataList = this.DataList.filter(t => t.id !== id)
   },
   addTask(task){
     this.DataList.push(task)
   }
  },
  components: {
  TaskList
  },
  data() {
    return {
      DataList: [
        {id:1, 
         title: 'Practice Javascript',
         completed: false
         },
         {
           id:2,
           title: 'Learn Laravel',
           completed: false
         },
         {
           id:3,
           title: 'Workout',
           completed: false
         }
      ]
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
  margin-top: 50px;
}

</style>
