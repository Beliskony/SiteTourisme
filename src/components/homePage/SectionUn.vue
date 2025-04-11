<template>
    <section class="w-full flex flex-row justify-around items-center max-sm:flex-col max-sm:gap-y-5">
      <div class="w-2/5 flex flex-col gap-y-5 justify-center items-center max-sm:w-full">
        <h2 class="text-5xl font-medium w-full max-sm:text-3xl max-sm:text-center">
          Decouvrer La Face Caché Du 
          <span 
            :style="{
              backgroundImage: `url(https://i.pinimg.com/736x/59/0f/4e/590f4ea536c092602ffe15f1045a1505.jpg)`,
              WebkitBackgroundClip: 'text',
              backgroundClip: 'text',
              color: 'transparent',
              backgroundSize: 'cover',
              backgroundPosition: 'center',
              WebkitTextStroke: '3px black'
            }" 
            class="text-5xl font-extrabold object-center max-sm:text-3xl"
          >
            Bénin
          </span>
        </h2>
        
        <p class="text-xs text-wrap w-full max-sm:px-1">
          Lorem ipsum dolor sit amet. Aut recusandae recusandae id facilis iusto et aliquam maiores qui quas dolor ut dolore voluptatibus 
          ea deleniti vero ea Quis animi. Nam odit consequatur est temporibus inventore ex eaque assumenda. Qui ipsa esse non saepe fugiat
          et laborum autem non iusto laboriosam ut nihil voluptatem vel exercitationem voluptas.
        </p>
      </div>
  
      <div class="w-2/5 gap-x-7 flex flex-row items-center justify-start max-sm:w-full">
        <div>
          <img 
            src="https://i.pinimg.com/474x/12/3a/25/123a259193e63b2c435c8b15b508274f.jpg" 
            class="rounded-2xl object-cover object-center h-[500px] w-[400px] max-sm:h-[300px] max-sm:[150px] max-sm:object-fill"
          />
        </div>
  
        <div class="flex flex-col gap-y-5">
          <img 
            src="https://i.pinimg.com/474x/68/6f/1d/686f1d01301b306401c202a8203e2e73.jpg" 
            class="rounded-2xl object-cover h-[250px] w-80 max-sm:h-[150px] max-sm:[100px] max-sm:object-fill"
          />
          <img 
            src="https://i.pinimg.com/474x/2f/3c/23/2f3c2373c9a942b000043a4c980a0941.jpg" 
            class="rounded-2xl object-cover h-[250px] w-80 max-sm:h-[150px] max-sm:[100px] max-sm:object-fill"
          />
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    name: 'SectionUn'
  }
  </script>