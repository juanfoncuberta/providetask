<template>
    <form class="mt-2 row justify-content-md-center">
        <InputAddTask />
        <button-add-task />
    </form>
</template>

<script>
import InputAddTask from './InputAddTask'
import ButtonAddTask from './ButtonAddTask'
import { provide, ref } from 'vue'
export default {
    components:{
        InputAddTask,
        ButtonAddTask
    },

    setup(){
        const taskList = ref([])
        var task = ref('')
        provide('taskList',taskList)
        provide('newTask',task)

    }
}
</script>
