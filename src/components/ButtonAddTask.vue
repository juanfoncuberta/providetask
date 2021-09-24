<template>
    <button type="button" class="btn btn-success col-9" @click="addToList">Add</button>
</template>

<script>
import { inject } from 'vue'
export default {
    setup(){

        const taskList = inject('taskList')
        const newTask = inject('newTask')
        
        const addToList = () =>  {
            if(newTask.value)
                console.log("ntvalue")
                console.log(newTask.value)
                var task = {
                    "id": taskList.value.length,
                    "name":newTask.value,
                    "done": 0
                }
                console.log("task")
                console.log(task);
                taskList.value.push(task)
                console.log(taskList.value.length)
            newTask.value = ''
        }

        return {addToList}
    }
}
</script>

<style>

</style>