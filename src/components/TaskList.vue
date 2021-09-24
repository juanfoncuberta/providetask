<template>
   <div class="row d mt-3 d-flex justify-content-center">
      <div 
        class="col-9" 
        v-for="(task,index) in taskList">
            <Card :task="task" :index="index" />
      </div>
  </div>
</template>

<script>
import Card from './TaskCard'
import { inject } from 'vue'
export default {
    components: {
        Card
    },    
    setup(){
        
        const taskList = inject('taskList')
        return {taskList}
    }
}
</script>
