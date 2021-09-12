<template>
   <div class="row">
      <div 
        class="col-12"
        v-for="task in taskList" :key="task">
            {{task}}
      </div>
  </div>
</template>

<script>
import { inject } from 'vue'
export default {

    setup(){
        
        const taskList = inject('taskList')
        return {taskList}
    }
}
</script>
