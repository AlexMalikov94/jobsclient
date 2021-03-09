<template>
    <div class="mt-10 flex justify-center">
        <form action="" class="w-6/12" @submit.prevent="login">
        <div class="mb-10">
           <h2 class="mb-4 text-2xl font-bold">Listing Details</h2>
           <div class="mb-4">
             <label for="job_title" class="inline-block mb-1 font-medium">Job Title</label>
             <input type="text" name="job_title" id="job_title" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.job_title">
           </div>
           <div class="mb-4">
             <label for="job_location" class="inline-block mb-1 font-medium">Job Location</label>
             <input type="text" name="job_location" id="job_location" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.job_location">
           </div>
           <div class="mb-4">
             <label for="job_link" class="inline-block mb-1 font-medium">Job application URL</label>
             <input type="text" name="job_link" id="job_link" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.job_link">
           </div>
           <div class="mb-4">
             <label for="tags" class="inline-block mb-1 font-medium">Tags</label>
             <input type="text" name="tags" id="tags" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.tags">
           </div>
           <div class="mb-4">
             <label for="company_name" class="inline-block mb-1 font-medium">Company Name</label>
             <input type="text" name="company_name" id="company_name" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.company_name">
           </div>
            <div class="mb-4">
             <label for="company_logo" class="inline-block mb-1 font-medium">Company logo URL</label>
             <input type="text" name="company_logo" id="company_logo" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.company_logo">
           </div>
           <div class="mb-4">
               <input type="checkbox" name="highlighted" id="highlighted" v-model="form.highlighted"><label for="highlighted">Highlighted listed</label>
           </div>
           <div class="mb-4">
               <input type="checkbox" name="pinned" id="pinned" v-model="form.pinned"><label for="pinned">Pinned</label>
           </div>
         </div>
           <div class="mb-10">
                 <h2 class="mb-4 text-2xl font-bold">Create an account to manage your listing</h2>
                 <div class="bg-gray-400 p-6 rounded-lg">
                    <div class="mb-4">
                        <label for="email" class="inline-block mb-1 font-medium">Email</label>
                        <input type="text" name="email" id="email" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.user_email">
                    </div>
                    <div class="mb-4">
                        <label for="name" class="inline-block mb-1 font-medium">Name</label>
                        <input type="text" name="name" id="name" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.user_name">
                    </div>
                    <div class="mb-4">
                        <label for="password" class="inline-block mb-1 font-medium">Password</label>
                        <input type="password" name="password" id="password" class="bg-gray-200 border-2 border-gray-200 rounded-lg w-full h-10 px-4" v-model="form.user_password">
                    </div>
                 </div>
           </div>
           <button type="submit" class="p-4 bg-blue-500 text-white font-medium rounded-lg">Create Listing</button>
        </form>
    </div>
</template>
<script>
export default {
    data() {
        return {
            form: {
                job_title: '',
                job_location: '',
                job_link: '',
                tags: [],
                company_name: '',
                company_logo: '',
                highlighted: false,
                pinned: false,
                user_name: '',
                user_email:'',
                user_password: ''
            }
        }
    }
}
</script>