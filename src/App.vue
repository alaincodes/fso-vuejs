<script setup>
import { reactive } from 'vue'
import Title from './components/Title.vue'
import Note from './components/Note.vue'

const courses = reactive([
  {
    name: 'Half Stack application development',
    id: 1,
    parts: [
      {
        name: 'Fundamentals of React',
        exercises: 10,
        id: 1
      },
      {
        name: 'Using props to pass data',
        exercises: 7,
        id: 2
      },
      {
        name: 'State of a component',
        exercises: 14,
        id: 3
      },
      {
        name: 'Redux',
        exercises: 11,
        id: 4
      }
    ]
  },
  {
    name: 'Node.js',
    id: 2,
    parts: [
      {
        name: 'Routing',
        exercises: 3,
        id: 1
      },
      {
        name: 'Middlewares',
        exercises: 7,
        id: 2
      }
    ]
  }
])
</script>

<template>
  <div v-for="course in courses" :key="course.id">
    <Title heading="h2" :text="course.name" />

    <ul>
      <Note
        v-for="name in course.parts"
        :key="name.id"
        :text="name.name"
        :exercise="name.exercises"
      />
    </ul>
  </div>
</template>
