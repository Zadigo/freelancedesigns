<template>
  <section>
    <section class="relative w-full h-screen min-h-187.5 bg-[#141414] text-white overflow-hidden font-sans select-none">
      <!-- Background Image & Subtle Vignette Overlay -->
      <div class="absolute inset-0 z-0">
        <nuxt-img src="/back/arch1.jpg" alt="Minimalist luxury dark wood kitchen island" class="w-full h-full object-cover object-center" />
        <!-- Top dark gradient for navbar legibility & bottom subtle shadow -->
        <div class="absolute inset-0 bg-linear-to-b from-[#141414]/90 via-black/15 to-[#141414]/60"></div>
      </div>
  
      <!-- Top Navigation Bar -->
      <header class="relative z-20 flex items-center justify-between px-8 md:px-14 py-7 text-[11px] tracking-[0.18em] uppercase font-medium">
        <!-- Left Navigation -->
        <nav class="flex items-center space-x-10 md:space-x-16">
          <nuxt-link to="#about" class="text-neutral-300 hover:text-white transition-colors">
            About
          </nuxt-link>
  
          <nuxt-link to="#collection" class="text-neutral-300 hover:text-white transition-colors">
            Collection
          </nuxt-link>
        </nav>
  
        <!-- Center Brand Logo -->
        <div class="flex items-start space-x-1.5">
          <!-- Geometric Boffi-style Emblem -->
          <div class="w-5 h-5 border-2 border-white flex items-center justify-center mt-0.5">
            <div class="w-2 h-2 bg-white"></div>
          </div>
          <span class="text-xl md:text-2xl font-bold tracking-tight lowercase leading-none">
            boffi
          </span>
          <span class="text-[11px] font-light tracking-tighter text-neutral-300 -mt-0.5">
            90<sup class="text-[7px] ml-0.5">yrs</sup>
          </span>
        </div>
  
        <!-- Right Navigation -->
        <nav class="flex items-center space-x-10 md:space-x-16">
          <nuxt-link to="#news" class="text-neutral-300 hover:text-white transition-colors">
            News
          </nuxt-link>
          
          <nuxt-link to="#project" class="text-neutral-300 hover:text-white transition-colors">
            Project
          </nuxt-link>
        </nav>
      </header>
  
      <!-- Center Display Typography -->
      <div class="relative z-10 flex flex-col items-center text-center mt-6 md:mt-10 px-4">
        <!-- Sub-caption -->
        <div class="flex items-center space-x-5 text-[11px] md:text-xs tracking-[0.14em] text-neutral-200 font-light mb-1">
          <span>Modern</span>
          <span class="w-1 h-1 rounded-full bg-white inline-block"></span>
          <span>Minimalist</span>
        </div>
  
        <!-- Oversized Hero Headline -->
        <h1 class="text-[16vw] md:text-[13.5rem] lg:text-[15.5rem] font-normal tracking-[-0.03em] leading-[0.88] text-white">
          Exquisite
        </h1>
      </div>
  
      <!-- Bottom Content Overlay (Description + Video Preview Card) -->
      <div class="absolute bottom-8 md:bottom-12 left-0 right-0 z-20 px-8 md:px-14 flex flex-col md:flex-row md:items-end justify-between gap-8">
        <!-- Bottom-Left Copy & CTA -->
        <div class="max-w-67.5 space-y-5">
          <p class="text-[11.5px] leading-[1.6] text-neutral-300 font-light">
            Boffi is dedicated to finding new approaches to interior living and functionalities to improve daily life in the home.
          </p>
  
          <nuxt-link to="#contact" class="inline-flex items-center space-x-2.5 border border-white/50 bg-[#141414]/40 backdrop-blur-xs px-4 py-2 text-[11px] tracking-wide text-white hover:bg-white hover:text-[#141414] transition-all duration-300 group">
            <span>Get In Touch</span>
            <span class="transform group-hover:translate-x-1 transition-transform duration-300">→</span>
          </nuxt-link>
        </div>
  
        <!-- Bottom-Right Video Thumbnail Card -->
        <button type="button" @click="isVideoOpen = true" aria-label="Play showcase video" class="relative w-64 sm:w-72 md:w-80 aspect-video overflow-hidden shadow-2xl border border-white/10 group cursor-pointer self-end">
          <nuxt-img src="https://unsplash.com" alt="Kitchen island video preview" class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500" />
          <div class="absolute inset-0 bg-black/25 group-hover:bg-black/15 transition-colors"></div>
  
          <!-- Translucent Play Button -->
          <div class="absolute inset-0 flex items-center justify-center">
            <div class="w-11 h-11 rounded-full bg-white/35 backdrop-blur-md flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
              <svg class="w-4 h-4 text-white fill-current ml-0.5" viewBox="0 0 24 24">
                <path d="M8 5v14l11-7z" />
              </svg>
            </div>
          </div>
        </button>
      </div>
  
      <!-- Optional Video Lightbox Modal -->
      <div v-if="isVideoOpen" @click.self="isVideoOpen = false" class="fixed inset-0 z-50 bg-black/85 backdrop-blur-sm flex items-center justify-center p-6">
        <div class="relative w-full max-w-4xl aspect-video bg-[#141414] border border-white/20 flex items-center justify-center">
          <u-button @click="isVideoOpen = false">
            Close ✕
          </u-button>
          <p class="text-sm text-neutral-400">Embed your architectural showcase video here</p>
        </div>
      </div>
    </section>

    <div class="p-20 h-200 bg-transparent text-white">
      <div class="grid grid-cols-12 gap-10">
        <div class="col-span-8">
          <div class="flex flex-col h-full justify-center">
            <motion :preset="VueUseMotions.SlideVisibleLeft" :duration="900">
              <h1 class="text-8xl font-bold max-w-2xl">
                The best website you can find
              </h1>
            </motion>
            
            <motion :preset="VueUseMotions.SlideVisibleRight" :duration="700">
              <p class="font-small text-light mt-10">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem odit dicta dignissimos quia a 
                dolore repellendus, sint vero aspernatur quis ipsa excepturi nobis fuga earum ex quisquam, illum amet. Repellat?
              </p>
            </motion>
          </div>
        </div>
        <div class="col-span-4">
          <p class="font-light">
            Some other text
          </p>
        </div>
      </div>
    </div>

    <div :style="{ background: 'url(/back/arch2.jpg)', backgroundRepeat: 'no-repeat', backgroundSize: 'cover', backgroundPositionY: '-300px'  }" class="overflow-hidden w-full h-150 my-3" />

    <div class="grid grid-cols-3 gap-3 text-white overflow-hidden">
      <lazy-archictecture-strip-three title="Accessoires" src="/back/arch2.jpg" rotation="-rotate-5" hydrate-on-idle />
      <lazy-archictecture-strip-three title="Accessoires" src="/back/arch3.jpg" rotation="rotate-0" hydrate-on-idle />
      <lazy-archictecture-strip-three title="Accessoires" src="/back/arch4.jpg" rotation="-rotate-5" hydrate-on-idle />
    </div>

    <footer class="flex flex-col md:flex-row gap-3 items-center justify-around w-full py-4 text-sm bg-transparent text-white mt-10">
      <p>Copyright © <nuxt-time :datetime="new Date()" year="numeric" /> PrebuiltUI. All rights reservered.</p>
      <div class="flex items-center gap-4">
        <nuxt-link to="/" class="hover:text-white transition-all">
          Contact Us
        </nuxt-link>

        <div class="h-8 w-px bg-white/20"></div>
        
        <nuxt-link to="/" class="hover:text-white transition-all">
          Privacy Policy
        </nuxt-link>
        
        <div class="h-8 w-px bg-white/20"></div>

        <nuxt-link to="/" class="hover:text-white transition-all">
          Trademark Policy
        </nuxt-link>
      </div>
    </footer>
  </section>
</template>

<script setup lang="ts">
// https://dribbble.com/shots/24612456-Boffi-Luxury-Minimalist-Modern-Interior-Design-Website-Main

const isVideoOpen = ref(false)

onMounted(() => {
  document.querySelector('body')?.classList.add('bg-[#141414]')
})
</script>

<style scoped>

</style>
