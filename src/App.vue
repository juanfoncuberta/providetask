<template>

  <NavBar />
  <FormAddTask />
  <TaskList />
  

</template>

<script>

import NavBar from './components/NavBar'
import FormAddTask from './components/FormAddTask'
import TaskList from './components/TaskList.vue'
export default {
  name: 'Provide Task',
  components: {
    NavBar,
    FormAddTask,
    TaskList
  }
}
</script>

<style>

</style>
