<template>
  <div
    :class="[task.reminder ? 'reminder' : '', 'task']"
    v-for="task in tasks"
    :key="task.id"
  >
    <h3>{{ task.title }}</h3>
    <p>{{ task.description }} 
      <i @click="$emit('delete-task', task.id)" class="fas fa-times"></i></p>
  </div>
</template>

<script>
export default {
  name: "TasksList",
  props: {
    tasks: Array,
  },
  emits: ['delete-task']
};
</script>

<style scoped>
.fa-times {
  color: red;
  float: right;
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.reminder {
  border-left: 5px solid green;
}
</style>