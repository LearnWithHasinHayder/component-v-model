<script setup>
import { ref, reactive } from 'vue'
import PersonComponent from './components/PersonComponent.vue'


const person = reactive({
  name: 'John Doe',
  email: 'john@doe.com'
})

</script>

<template>
  <div class="container mx-auto">
    <div class="flex items-center mt-5">
      <img class="logo" src="./assets/vue.svg" alt="Vue logo" />
      <h1 class="text-2xl">Component Model</h1>
    </div>

    <div class="mt-10">
      Original Name: {{ person.name }}<br/>
      Original Email: {{ person.email }}
    </div>

    <div class="mt-10">
      <label>Name</label>
      <p>
        <input type="text" v-model="person.name" />
      </p>
    </div>

    <div class="mt-10">
      <label>Component</label><br />
      <PersonComponent :person="person" />
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  padding-left: 0;
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
