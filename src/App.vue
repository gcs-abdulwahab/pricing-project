<script setup>
import { ref } from 'vue';

import PriceComponent from './components/PriceComponent.vue';
import ToggleComponent from './components/ToggleComponent.vue';
 
const Items = [
  {
    id: 1,
    offerTag: "Basic",
    price: 129,
    selected: false,
    features: [
      { name: "Unlimited updates", value: true },
      { name: "Git repository", value: true },
      { name: "npm installation", value: true },
      { name: "Unlimited users", value: true },
      { name: "Unlimited projects", value: false },
      { name: "Unlimited storage", value: false },
      { name: "Unlimited bandwidth", value: true },
      { name: "Unlimited support", value: false },
    ],
  },
  {
    id: 2,
    offerTag: "Premium",
    price: 249,
    selected: true,
    features: [
      { name: "Unlimited updates", value: true },
      { name: "Git repository", value: true },
      { name: "npm installation", value: true },
      { name: "Unlimited users", value: true },
      { name: "Unlimited projects", value: true },
      { name: "Unlimited storage", value: true },
      { name: "Unlimited bandwidth", value: true },
      { name: "24/7 support", value: true },
    ],
  },
  {
    id: 3,
    offerTag: "Enterprise",
    price: 499,
    selected: false,
    features: [
      { name: "Unlimited updates", value: true },
      { name: "Git repository", value: true },
      { name: "npm installation", value: true },
      { name: "Unlimited users", value: true },
      { name: "Unlimited projects", value: true },
      { name: "Unlimited storage", value: false },
      { name: "Unlimited bandwidth", value: true },
      { name: "Dedicated account manager", value: false },
      { name: "Custom SLA", value: true },
      { name: "Custom features", value: false },
      { name: "Dedicated account manager", value: false },
      { name: "Custom SLA", value: true },
      { name: "Custom features", value: false },
      { name: "Dedicated account manager", value: false },
      { name: "Custom SLA", value: true },
      { name: "Custom features", value: false },
    ],
  },
];


const items = ref(Items);


</script>

<template>
  <div class="container mx-auto bg-red-400 text-center  py-4 flex flex-col">
    <h1 class="font-bold mb-2 text-2xl    dark:text-white  "> Pricing</h1>
    <ToggleComponent />
       
    <section id="pricing" class="bg-blue-200 h-auto flex  flex-col md:flex-row  
    items-center   mt-2 p-2  justify-around">

      
      <PriceComponent class="mb-2 w-full  " v-for="item in items" :key="item.id" :item="item" />



    </section>
    
  </div>
</template>