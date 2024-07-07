<script setup>
const props = defineProps({
  id: {
    type: Number
  },
  important: {
    type: Boolean
  },
  text: {
    type: String,
    required: true
  },
  exercise: {
    type: Number,
    default: 0
  }
})
</script>

<template>
  <li>{{ props.text }}: {{ props.exercise }}</li>
</template>
