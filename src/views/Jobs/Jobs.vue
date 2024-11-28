<template>
  <h1>Jobs</h1>
  <div class="jobs" v-for="job in jobs" :key="job.id">
    <router-link :to="{name:'JobDetail',params:{id:job.id}}">
    <h1>{{job.title}}</h1>
    </router-link>
  </div>
</template>

<script>
export default {
    data(){
        return{
            jobs:[
               
            ]
        }
    },
    mounted(){
      fetch('http://localhost:3000/jobs')
    }
}
</script>

<style>
 .jobs{
    color: crimson;
 }
</style>