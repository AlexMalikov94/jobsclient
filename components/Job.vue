<template>
    <div class="border-b-2 border-t-2 border-gray-200  p-4 pb-2 flex justify-between group">
        <img :src="job.company_logo" :alt="`${job.company_name} logo`" class="h-12 w-12 mr-4">
        <div class="flex items-center justify-between w-full">
            <div class="w-full md:w-4/12 mb-2">
                <h2 class="font-bold leading-none">{{ job.job_title }}</h2>
                <a href="#" class="text-sm">{{  job.company_name }}</a>
                <div class="flex items-center">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" class="w-4 h-4 text-gray-600 mr-1">
                    <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" />
                    </svg>
                    <div class="text-sm text-gray-600">
                        {{ job.job_location }}
                    </div>
                </div>
            </div>
            <div class="w-full md:w-4/12 mb-2">
                <a href="" v-for="tag in job.tags" :key="tag.slug" class="inline-block text-gray-600 border-2 border-gray-300 px-3 py-1 rounded-lg mr-2 bg-white">{{ tag.title }}</a>
            </div>
            <div>
                <div class="opacity-100 md:opacity-0 group-hover:opacity-100 transition-opacity duration-200">
                     <a :href="job.job_link" class="inline-block border-2 border-blue-400 text-blue-400 font-bold rounded-lg px-3 py-2 bg-white">Apply for this job</a>
                </div>
               
            </div>
        </div>
    </div>
</template>
<script>
export default {
   props: {
       job: {
           required: true,
           type: Object
       }
   } 
}
</script>
