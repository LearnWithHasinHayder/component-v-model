<script setup>
import { ref, reactive } from 'vue'

import Radio from './components/Radio.vue';


const fruit = ref('apple')

const fname = ref('John')
const lname = ref('Doe')

</script>

<template>
  <div class="container mx-auto">
    <div class="flex items-center mt-5">
      <img class="logo" src="./assets/vue.svg" alt="Vue logo" />
      <h1 class="text-2xl">Component Model</h1>
    </div>

    <div class="mt-10">
      Fruit: {{ fruit }}<br />
    </div>

    <div class="mt-10">
      <label>Component</label><br />
      <p class="mt-5">
        <label> Your favorite fruit</label> <br />
        <Radio v-model="fruit" label="Apple" value="apple" />
        <Radio v-model="fruit" label="Banana" value="banana" />
        <Radio v-model="fruit" label="Orange" value="orange" />
      </p>

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
