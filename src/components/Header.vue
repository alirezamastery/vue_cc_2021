<template>
  <header>
    <h1>Task tracker</h1>
    <h1>{{title}}</h1>
    <Button @btn-click="$emit('toggle-add-task')"
            :text="showAddTask ? 'close' : 'Add Task'"
            :color="showAddTask ? 'red' : 'green'" />
<!--    <Button text="update task" color="blue"/>-->
<!--    <Button text="delete task" color="red"/>-->
  </header>
</template>

<script>
import Button from "@/components/Button";
export default {
  name:'Header',
  props: {
    title: String,
    showAddTask:Boolean
  },
  components:{
    Button,
  }
}
</script>