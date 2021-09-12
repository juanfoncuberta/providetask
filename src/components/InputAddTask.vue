<template>
    <div class="form-group col-9 ">
        <label for="addTask">Add Task:</label>
        <input  v-model="newTask" type="text" class="form-control" id="newTask" placeholder="Add a task">
  </div>
</template>

<script>
import { inject  } from 'vue'
export default {

    setup(){        
        
        const newTask = inject('newTask')
        return {newTask}
    }
}
</script>
