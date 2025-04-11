<template>
    <div class="embla w-full justify-center items-center my-5 overflow-hidden" ref="emblaRef">
      <div class="embla__container flex gap-5">
        <div 
          v-for="item in popularite" 
          :key="item.id" 
          class="embla__slider flex-shrink-0 w-[250px] hover:gap-y-2"
        >
          <img 
            :src="item.imageRep" 
            :alt="item.titre" 
            class="w-full h-[350px] object-cover rounded-2xl hover:my-2 hover:scale-110 transition-all ease-in-out"
          />
          <div class="flex flex-col p-2 text-left text-wrap">
            <h3 class="text-lg font-semibold text-black">{{ item.titre }}</h3>
            <a href="#"><p class="text-sm text-gray-600">{{ item.localisation }}</p></a>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import { ref, onMounted } from 'vue'
  import useEmblaCarousel from 'embla-carousel-vue'
  import Autoplay from 'embla-carousel-autoplay'
  
  export default {
    name: 'Musee',
    setup() {
      const popularite = [
        {id: 1, titre: "Porte du non retour", localisation: "Ouidah", imageRep: "https://i.pinimg.com/736x/e4/fc/a7/e4fca707f3e58004a55d987b79ccd67c.jpg"},
        {id: 2, titre: "Temple des Pythons", localisation: "Ouidah", imageRep: "https://lh3.googleusercontent.com/gps-cs-s/AB5caB-jjbG3rlVTnA8AzebDmVoL_jFs8gKnPKTkK1BYMXyJwGnPNVltRiGlE0De1jioloFmUQ0rlc4EBLS9hR8-eDCu-ppjnVCvqEI3dyAK3yhDLKJUlcxh6KceU8X8pofULuUz8B2n=s1360-w1360-h1020-rw"},
        {id: 3, titre: "Parc National de la Pendjari", localisation: "Porto-Novo", imageRep: "https://i.pinimg.com/736x/3c/10/d8/3c10d881bd15f1ca5a38225ac4accc50.jpg"},
        {id: 4, titre: "Musée Honmè", localisation: "Atakora", imageRep: "https://i.pinimg.com/736x/a4/39/a6/a439a6ef88ebf0ad42204f6f13968552.jpg"},
        {id: 5, titre: "Place des Amazones", localisation: "Cotonou", imageRep: "https://i.pinimg.com/474x/26/c1/ea/26c1ea302dd87b609c49ebb44e8aec0a.jpg"},
        {id: 6, titre: "Marché Dantokpa", localisation: "Cotonou", imageRep: "https://i.pinimg.com/474x/97/ec/08/97ec0871aaf12cce85456172075dad46.jpg"},
      ]
  
      const emblaRef = ref(null)
      
      onMounted(() => {
        const autoplayOption = {
          delay: 5000,
        }
        
        useEmblaCarousel(
          emblaRef.value, 
          {loop: false, align: 'start', containScroll: 'trimSnaps'}, 
          [Autoplay(autoplayOption)]
        )
      })
  
      return {
        popularite,
        emblaRef
      }
    }
  }
  </script>