<template>
   <div class="row d mt-3 d-flex justify-content-center">
      <div 
        class="col-9" 
        v-for="task in taskList" :key="task">
            <div class="alert alert-warning" role="alert">
                    {{task}}
            </div>
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
