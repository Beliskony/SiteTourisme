<template>
    <section class="bg-transparent w-full h-16 backdrop-blur-lg flex items-center">
      <nav class="sm:px-6 lg:px-8 w-full justify-around flex flex-row absolute">
        <!-- Logo -->
        <div class="flex items-center text-3xl text-black font-bold w-1/6 justify-start">
          <RouterLink to="/">
            <img src="/images/boursol.png" class="h-24 w-24" />
          </RouterLink>
        </div>
  
        <!-- Menu Desktop -->
        <div class="max-sm:hidden flex flex-row w-4/6 items-center justify-center">
          <RouterLink
            to="/"
            class="block py-2 px-4 text-black text-sm hover:text-2xl hover:font-bold"
          >
            Acceuil
          </RouterLink>
  
          <RouterLink
            to="/Services"
            class="block py-2 px-4 text-black hover:text-2xl hover:font-bold"
          >
            Servcice
          </RouterLink>
  
          <RouterLink
            to="/Apropos"
            class="block py-2 px-4 text-black hover:text-2xl hover:font-bold"
          >
            A propos
          </RouterLink>
  
          <RouterLink
            to="/Contacts"
            class="block py-2 px-4 text-black hover:text-2xl hover:font-bold"
          >
            Contacts
          </RouterLink>
  
          <RouterLink
            to="/Produits"
            class="block py-2 px-4 text-black hover:text-2xl hover:font-bold"
          >
            Produits
          </RouterLink>
        </div>
  
        <!-- Search + SignIn -->
        <div class="max-sm:hidden flex flex-row w-2/6 items-center justify-between gap-x-1">
          <div class="flex flex-row justify-center items-center gap-1 w-48">
            <img src="/icones/search.svg" class="h-5 w-5" />
            <input type="text" placeholder="recherche" class="w-full focus:outline-none" />
          </div>
  
          <div class="flex w-32">
            <button
              @click="openForm = true"
              class="flex bg-black text-xl text-white justify-center items-center rounded-3xl p-2 w-full"
            >
              SignIn
            </button>
            <div v-if="openForm">
              <!-- Ajouter le formulaire ici -->
            </div>
          </div>
        </div>
  
        <!-- Menu Mobile -->
        <button
          class="flex flex-col items-center justify-center lg:hidden md:hidden text-black z-50"
          @click="isOpen = !isOpen"
        >
          <img
            v-if="isOpen"
            src="/icones/close.svg"
            class="absolute right-2 w-20 h-20 z-50"
          />
          <img
            v-else
            src="/icones/menu.svg"
            class="w-8 h-8"
          />
  
          <Transition name="fade">
            <div
              v-if="isOpen"
              class="md:hidden bg-white shadow-md fixed top-0 left-0 w-screen h-screen flex flex-col pt-28 z-40"
            >
              <RouterLink
                to="/"
                class="block py-2 px-4 text-[#1E0F1C] hover:text-2xl hover:font-bold"
              >
                Acceuil
              </RouterLink>
  
              <RouterLink
                to="/Services"
                class="block py-2 px-4 text-[#1E0F1C] hover:text-2xl hover:font-bold"
              >
                Servcice
              </RouterLink>
  
              <RouterLink
                to="/Apropos"
                class="block py-2 px-4 text-[#1E0F1C] hover:text-2xl hover:font-bold"
              >
                A propos
              </RouterLink>
  
              <RouterLink
                to="/Contacts"
                class="block py-2 px-4 text-[#1E0F1C] hover:text-2xl hover:font-bold"
              >
                Contacts
              </RouterLink>
  
              <RouterLink
                to="/Produits"
                class="block py-2 px-4 text-[#1E0F1C] hover:text-2xl hover:font-bold"
              >
                Produits
              </RouterLink>
            </div>
          </Transition>
        </button>
      </nav>
    </section>
  </template>
  
  <script lang="ts" setup>
  import { ref } from 'vue'
  
  const isOpen = ref(false)
  const openForm = ref(false)
  </script>
  
  <style scoped>
  .fade-enter-active,
  .fade-leave-active {
    transition: all 0.3s ease;
  }
  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
    transform: translateY(-10px);
  }
  </style>
  