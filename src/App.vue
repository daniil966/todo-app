<script setup>
import TaskItem from './components/TaskItem.vue'

const tasks = [
  {
    id: 1,
    title: 'Сходить в магазин',
    text: 'Купить продукты на неделю'
  },
  {
    id: 2,
    title: 'Забрать посылку',
    text: 'Забрать заказ из пункта выдачи'
  },
  {
    id: 3,
    title: 'Отнести вещи в химчистку',
    text: 'Сдать зимнюю одежду на чистку'
  }
]
</script>

<template>
  <div class="app">
    <h1>Список дел</h1>
    <div class="tasks">
      <TaskItem
        v-for="task in tasks"
        :key="task.id"
        :task="task"
      />
    </div>
  </div>
</template>

<style scoped>
.app {
  padding: 20px;
  font-family: Arial, sans-serif;
}
.tasks {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}
</style>