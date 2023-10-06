<script setup>
 const props = defineProps({
      name:String,
      modelValue:Boolean
      
 })

 defineEmits(['update:modelValue'])

</script>
 
<template>
<input type="checkbox" :checked="modelValue" @input="$emit('update:modelValue', !modelValue)">
{{ name }}
</template>
 
<style scoped>
 
</style>