<template>
    <header class="py-6 flex items-center justify-between">
        <nuxt-link :to="{ name: 'index'}" exact-active-class="text-blue-500">Jobs</nuxt-link>
        <div class="-mx-4 flex item-center flex-wrap">
            <template v-if="$auth.loggedIn">
            <nuxt-link :to="{ name: 'jobs-create' }" class="mx-4" exact-active-class="text-blue-500">Post a job</nuxt-link>
            <span class="mx-4 font-bold" exact-active-class="text-blue-500">{{  $auth.user.name }}</span>
            <nuxt-link :to="{name: 'user-listings'}" class="mx-4" exact-active-class="text-blue-500">Manage Listings</nuxt-link>
            <a href="" class="mx-4" exact-active-class="text-blue-500" @click.prevent="logout">Logout</a>
            </template>
            <template v-if="!$auth.loggedIn">
            <nuxt-link :to="{ name: 'jobs-create' }" class="mx-4" exact-active-class="text-blue-500">Post a job</nuxt-link>
            <nuxt-link :to="{ name: 'login'}" class="mx-4" exact-active-class="text-blue-500">Login</nuxt-link>
           
      
            </template>
      
          
        </div>
    </header>
</template>
<script>
export default {
    methods: {
        async logout() {
           await this.$auth.logout();
           this.$router.replace({ name: 'index'})
        }
     }
}
</script>