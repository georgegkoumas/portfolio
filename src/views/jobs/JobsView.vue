<template>
    <h1>This is the jobs page</h1>
      <div v-for="job in jobs" :key="jobs.id" class="job">
      <router-link :to="{ name: 'JobDetails' , params: { id: job.id}}">
        <h2>{{  job.title }}</h2>
      </router-link>
    </div>
  </template>

<script>  
  export default {
    data() {
      return {
        jobs: [
          { title: 'UX Designer' , id: 1, details: 'lorem'},
          { title: 'Web Designer' , id: 2, details: 'lorem'},
          { title: 'Vue Designer' , id: 3, details: 'lorem'},
          { title: 'Network Administrator' , id: 4, details: 'lorem'},
          { title: 'Systems Administrator' , id: 5, details: 'lorem'},
          { title: 'Data Center Technician' , id: 6, details: 'lorem'},
          { title: 'Help Desk L1-3' , id: 7, details: 'lorem'},
        ]
      }
    }
  }
</script>

<style>
.job h2{
  background: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h2:hover {
  background: #ddd;  
}
.job a{
  text-decoration: none;
}
</style>