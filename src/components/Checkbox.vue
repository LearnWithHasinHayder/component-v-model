<script setup>
const props = defineProps([
    'label', 'modelValue'
])

const emit = defineEmits(['update:modelValue'])
</script>
 
<template>
    <!-- @change="$emit('update:modelValue',!modelValue)" -->
    <p>
        <label>{{ label }}</label> 
        <input 
            class="ml-5" 
            type = "checkbox" 
            :checked="modelValue"
            @change="$emit('update:modelValue',$event.target.checked)"
            
            />
    </p>
</template>
 
<style scoped></style>