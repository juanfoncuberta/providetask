<template>
    <!-- <div class="justify-content-center col-9"> -->
    <button type="button" class="btn btn-success col-9" @click="addToList">Add</button>
    <!-- </div> -->
</template>

<script>
import { inject } from 'vue'
export default {
    setup(){

        const taskList = inject('taskList')
        const newTask = inject('newTask')
        
        const addToList = () =>  {
            taskList.value.push(taskList.value)
        }

        return {addToList}
    }
}
</script>

<style>

</style>