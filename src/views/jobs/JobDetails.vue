<template>
  <h1>Job details views here</h1>
  <p>The job id is {{ $route.params.id }}</p>
</template>

<script>
export default {
    data(){
        return{
            id: this.route.params.id,
        }
    },
    props:['id']
}
</script>

<style>

</style>