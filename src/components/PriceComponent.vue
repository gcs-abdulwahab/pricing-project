<script setup >

import { defineProps } from 'vue';
const props = defineProps({
    item: Object,
    required: true,  
})
    
</script>


<template>
   
   <div class="bg-white flex flex-col  space-y-2 p-2  rounded-2xl shadow-2xl 
   
   
   " >
        <h1 class="uppercase text-2xl font-bold "> {{ item.offerTag }}</h1>
        <h2 class="font-semibold" > ${{ item.price}} / Year</h2>
        <button type="button" class="font-bold text-blue-700 bg-gray-300 
        hover:text-white
        hover:bg-blue-800 focus:ring-4 focus:ring-blue-300 rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 dark:bg-blue-600 dark:hover:bg-blue-700 focus:outline-none dark:focus:ring-blue-800 uppercase">buy</button>
        <hr/>
        <ul class="flex flex-col bg-white p-5 list-none items-start">            
            <li  v-for="(feature, index) in item.features" :key="index"
             class="truncate ">
             
             <i class="px-2 fas fa-check-circle text-green-500"
                :class="feature.value ? 'text-green-500 ' : 'text-red-500  fa-times-circle '"            
             ></i>
             
             
             
             {{ feature.name }} 
            
            </li>
            
             
      
        </ul>        
    </div>
</template>