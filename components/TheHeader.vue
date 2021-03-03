<template>
    <header class="py-6 flex items-center justify-between">
        <nuxt-link :to="{ name: 'index'}" exact-active-class="text-blue-500">Jobs</nuxt-link>
        <div class="-mx-4 flex item-center flex-wrap">
            <span class="mx-4 font-bold" exact-active-class="text-blue-500">Alex</span>
            <nuxt-link :to="{ name: 'login'}" class="mx-4" exact-active-class="text-blue-500">Login</nuxt-link>
            <a href="" class="mx-4" exact-active-class="text-blue-500">Manage Listings</a>
            <a href="" class="mx-4" exact-active-class="text-blue-500">Logout</a>
            <a href="" class="mx-4" exact-active-class="text-blue-500">Post a job</a>
        </div>
    </header>
</template>