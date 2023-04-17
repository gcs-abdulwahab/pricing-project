<script setup>
import ToggleComponent from './components/ToggleComponent.vue';

import PriceComponent from './components/PriceComponent.vue';


</script>

<template>
  <div class="container mx-auto bg-red-400 text-center  py-4 ">
    <h1 class="font-bold mb-4"> Pricing</h1>
    <ToggleComponent />
   
    <section id="pricing" class="bg-blue-200 h-96">
   
      <PriceComponent />


    </section>
  </div>
</template>