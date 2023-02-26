<template>
  <div>
    <img src="./assets/logo.png" alt="Vue logo">
    <SchoolStudent></SchoolStudent>
    <SchoolSchool></SchoolSchool>
  </div>
</template>

<script>
// 引入组件
import SchoolSchool from './components/SchoolSchool.vue'
import SchoolStudent from './components/SchoolStudent.vue'

export default {
    name: "App",
    components: { 
      SchoolStudent,
      SchoolSchool
      }
}
</script>

<style>

</style>