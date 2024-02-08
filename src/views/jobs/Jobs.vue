<template>
  <h1>Jobs</h1>
  <div class="job" v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'jobsDetails', params:{ id: job.id }}">
      <h2>{{ job.title }}</h2>
    </router-link>
  </div>
</template>

<script>
export default {
    data(){
        return{
            jobs:[
                {title:'Ninja Ux Designer', id:1, details:'lorem'},
                {title:'Ninja Web Developer', id:2, details:'lorem'},
                {title:'Ninja vue Developer',id:3,details:'lorem'}
            ]
        }
    }
}
</script>

<style>
.job h2{
  background: #f4f4f4;
  padding: 20px;
  border-radius: 20px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h2:hover{
  background: #fff;
}
.job a{
  text-decoration: none;
}
</style>