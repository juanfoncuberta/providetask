<template>
  <NavBar />
    <div class="justify-content-md-center">
  <FormAddTask />
  <TaskList />
    </div>
  

</template>

<script>

import NavBar from './components/NavBar'
import FormAddTask from './components/FormAddTask'
import TaskList from './components/TaskList.vue'
import { provide, ref } from 'vue'
export default {
  name: 'Provide Task',
  components: {
    NavBar,
    FormAddTask,
    TaskList
  },
  setup(){
    const taskList = ref([])
    
    var task = ref('')
    provide('taskList',taskList)
    provide('newTask',task)

  }
}
</script>

<style>

</style>
