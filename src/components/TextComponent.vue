<script setup>
const props = defineProps([
    'label','name','person'
])
// const emit = defineEmits(['update:modelValue'])
</script>
 
<template>
<div class="my-5">
    <label>{{ label }}</label>
    <p>
        <!-- <input type="text" :value="modelValue" @input="$emit('update:modelValue', $event.target.value)" /> -->
        <input type="text" v-model="person.name" />
    </p>
</div>
</template>
 
<style scoped>
 
</style>