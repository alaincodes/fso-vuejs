<!-- eslint-disable vue/multi-word-component-names -->
<script setup>
const props = defineProps({
  text: {
    type: String,
    required: true
  },
  id: {
    type: Number
  },
  heading: {
    type: String,
    default: 'h2'
  }
})
</script>

<template>
  <component :is="heading" :id class="text-3xl font-bold">{{ props.text }}</component>
</template>
