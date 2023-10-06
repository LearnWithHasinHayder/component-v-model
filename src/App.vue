<script setup>
import { ref, reactive } from 'vue'
import TextComponent from './components/TextComponent.vue';
import Task from './components/Task.vue';
import TaskModel from './components/TaskModel.vue';

const name = ref('John Doe')

const person = reactive(
  {
    name: 'John Doe',
    age: 30,
    location: 'Earth'
  }
)

const task = ref({
  name: 'Learn Vue',
  done: false
})
</script>

<template>
  <div class="container mx-auto">
    <div class="flex items-center mt-5">
      <img class="logo" src="./assets/vue.svg" alt="Vue logo" />
      <h1 class="text-2xl">Component Model</h1>
    </div>

    <div class="mt-10">
      {{ person }}
    </div>

    <div class="mt-10">
      <h1>Root</h1>
      <label>Name</label>
      <p>
        <input type="text" v-model="name" />
      </p>
    </div>

    <div class="mt-10">
      <h1>Component</h1>
      <TextComponent label="Name" :person="person" />
    </div>

    <div class="mt-10">
      {{ task }}
      <h1>Task Component</h1>
      <Task :task="task" />
    </div>

    <div class="mt-10">
      {{ task }}
      <h1>Task Component</h1>
      <TaskModel v-model="task.done" :name="task.name" />
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
