<template>
  <CourseIndex msg="Video course" :course="course"/>
</template>

<script>
import CourseIndex from '@/components/CourseIndex.vue'
//import ListLessons from '@/ListLessons.js'
import { Course } from '@/ListLessons.js'

export default {
  components: {
    CourseIndex
  },
  name: 'App',
  data() {
    return {
      course: [],
    }
  },
  mounted() {
    this.course = Course;
    console.log(this.course);
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
