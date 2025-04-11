<template>
    <section class="flex flex-col w-full p-5">
      <h1 class="text-4xl font-bold text-black">Top Destinations</h1>
      <SwitchDestination />
    </section>
  </template>
  
  <script>
  import SwitchDestination from './SwitchDestination.vue'
  
  export default {
    name: 'TopDestination',
    components: {
      SwitchDestination
    }
  }
  </script>