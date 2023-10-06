<script setup>
 const props = defineProps([
     'task'
 ])

</script>
 
<template>
<input type="checkbox" v-model="task.done">
{{ task.name }}
</template>
 
<style scoped>
 
</style>