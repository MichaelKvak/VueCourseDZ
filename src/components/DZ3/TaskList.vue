<template>
    <div>
<h1>Task List</h1>
<form @submit.prevent="onSubmit">
<input type="text" v-model="title">
</form>


<div>
    <span class="NumArray">
     {{DataList.length}} Tasks
   </span>
  
         <li v-for="(task,i) of DataList" :key="task.id" 
             
             v-bind:class="{done: task.completed}" 
             v-bind:index="i"
             v-on:remove-task="removeTask"
             
             >
             <strong>
                 {{i+1}}
                    <span class="space">
                        {{task.title}} 
                    </span>
             </strong>  
                <span >
                    <button class="btm" v-on:click ="task.completed = !task.completed">&#9998;</button>
                    <button class="btn" v-on:click ="$emit('remove-task', task.id)"> &times; </button>
                </span>
               
         </li>
         
</div>
   

    </div>
</template>

<script>
    export default {
        name: 'TaskList',
        data() {
            return {
            task: 0,
            title: '',
            
            }
        },
        props: {
            DataList: {
                type: Array,
                default: ()=>[],
                
        },
        index: Number,
        
        
        },
        methods: {
            removeTask(id) {
                this.$emit('remove-task', id)

            },

            onSubmit() {
                    if(this.title.trim()){
                    const newTask = {
                        id: Date.now(),
                        title: this.title,
                        completed: false
                    }
                    this.$emit('add-task', newTask)
                    this.title=""
                }

            },
           

              
        }

    }
</script>

<style lang="css" scoped>
li{
    list-style: none;
    margin: 0;
    padding: 0;
    border: 1px solid #ccc;
    display: flex;
    justify-content: space-between;
    padding: .5rem 2rem;
    margin-bottom: 1rem;
}
.btn{
    margin-left: 10px;
   background: linear-gradient(150deg, rgb(252, 2, 2) 0%, rgb(245, 244, 245) 100%);
   color: #FFF;
   border-radius: 50%;
   font-weight: bold; 
}
.btm{
 
        background: linear-gradient(150deg, rgb(5, 5, 5) 0%, rgb(245, 244, 245) 100%);
        color: #FFF;
        border-radius: 50%;
        font-weight: bold; 
}
.space{
    padding: 20px;
}
.done{
    text-decoration: line-through;
}
.NumArray{
    display: flex;
    margin-bottom: 20px;
    margin-left: 50px;
    font-weight: bold
}
input {
    width: 250px;
    margin: 25px;
}

</style>