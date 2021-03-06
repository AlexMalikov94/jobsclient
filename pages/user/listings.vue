<template>
<div>
  <div class="text-center py-10">
    <h1 class="text-4xl font-bold mb-2">Your Listings.</h1>
  </div>
  <div class="mt-10" v-if="me">
    <job v-for="job in me.jobs" :key="job.id" :job="job"></job>
  </div>   
</div>
</template>

<script>
//import Job from '../components/Job.vue';
import USER_JOBS from '@/graphql/UserJobs.gql';
export default {
  apollo: {
     me: {
       query: USER_JOBS,
       fetchPolicy: 'network-only',
       prefetch: false
     }
  }
}
</script>

<style>

</style>
