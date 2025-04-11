<template>
    <div class="flex flex-col w-full gap-x-1.5 items-center py-2 max-sm:gap-x-0.5">
      <div class="my-3 flex flex-row justify-around w-full max-sm:flex-col">
        <div class="flex flex-row justify-center gap-x-5 items-center w-3/4 max-sm:gap-x-1 max-sm:w-full max-sm:text-xs">
          <button @click="type = 1" :class="type === 1 ? 'font-bold' : 'no-underline'">
            <h3>Populaires</h3>
          </button>
  
          <button @click="type = 2" :class="type === 2 ? 'font-bold' : 'no-underline'">
            <h3>Coline of tears</h3>
          </button>
  
          <button @click="type = 3" :class="type === 3 ? 'font-bold' : 'no-underline'">
            <h3>Cultural complex</h3>
          </button>
  
          <button @click="type = 4" :class="type === 4 ? 'font-bold' : 'no-underline'">
            <h3>Musee National</h3>
          </button>
  
          <button @click="type = 5" :class="type === 5 ? 'font-bold' : 'no-underline'">
            <h3>Vodoo festival</h3>
          </button>
        </div>
  
        <div class="justify-center items-center w-1/4 max-sm:hidden">
          <div class="w-60 text-center py-1 px-5 text-xl font-medium border rounded-3xl text-black hover:text-white hover:bg-black">
            <a href="#">
              <h3>Voir tous</h3>
            </a>
          </div>
        </div>
      </div>
  
      <div class="flex flex-row w-full justify-center items-center">
        <component :is="currentComponent" />
      </div>

      <div class="justify-center items-center w-2/4 md:hidden lg:hidden xl:hidden">
          <div class="w-60 justify-center items-center text-center py-1 px-5 text-xl font-medium border rounded-3xl text-black hover:text-white hover:bg-black">
            <a href="#">
              <h3>Voir tous</h3>
            </a>
          </div>
        </div>
    </div>
  </template>
  
  <script>
  import { ref, computed } from 'vue'
  import Populaires from './groupesDestinations/Populaires.vue'
  import Coline from './groupesDestinations/Coline.vue'
  import Cultural from './groupesDestinations/Cultural.vue'
  import Musee from './groupesDestinations/Musee.vue'
  import Vodoo from './groupesDestinations/Vodoo.vue'
  
  export default {
    name: 'SwitchDestination',
    components: {
      Populaires,
      Coline,
      Cultural,
      Musee,
      Vodoo
    },
    setup() {
      const type = ref(1)
  
      const currentComponent = computed(() => {
        switch (type.value) {
          case 1:
            return Populaires
          case 2:
            return Coline
          case 3:
            return Cultural
          case 4:
            return Musee
          case 5:
            return Vodoo
          default:
            return Populaires
        }
      })
  
      return {
        type,
        currentComponent
      }
    }
  }
  </script>