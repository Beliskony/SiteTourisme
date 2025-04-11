<script setup lang="ts">
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import TopDestination from './components/homePage/TopDestination.vue';
import SectionUn from './components/homePage/SectionUn.vue';

</script>

<template>
  <section>
    <!--Header-->
    <div>
      <Header />
    </div>

    <!--Corps-->
    <div className='h-full w-full p-5 gap-y-5 flex flex-col max-sm:px-0.5'>
          <SectionUn />

          <TopDestination />
    </div>
    
    <!--Footer-->
    <div>
      <Footer />
    </div>
    
  </section> 
</template>
