<script setup>
defineProps({
  task: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <div class="task-item">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<style scoped>
.task-item {
  border: 1px solid #ccc;
  border-radius: 8px;
  padding: 16px;
  background-color: #f9f9f9;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}
.task-item h3 {
  margin: 0 0 8px;
  color: #333;
}
.task-item p {
  margin: 0;
  color: #666;
}
</style>