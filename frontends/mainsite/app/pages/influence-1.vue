<template>
  <section>
    <div :style="{ background: `url(/back/infl1.jpg)`, backgroundPosition: 'center', backgroundSize: 'cover' }" class="w-full h-screen relative">
      <nav class="relative w-full p-6 md:p-16 lg:p-16 xl:p-10 flex items-center justify-start gap-10 z-20 bg-transparent text-[#f1e5a2] transition-all">
        <nuxt-link href="/" class="text-[#f1e5a2] font-bold text-4xl uppercase">
          Some Design
        </nuxt-link>

        <div class="flex justify-between w-[75%]">
          <ul class="md:flex hidden items-center gap-10 text-xl font-semibold">
            <li><nuxt-link class="hover:text-[#f1e5a2]/80 transition" href="#">Home</nuxt-link></li>
            <li><nuxt-link class="hover:text-[#f1e5a2]/80 transition" href="#">Services</nuxt-link></li>
            <li><nuxt-link class="hover:text-[#f1e5a2]/80 transition" href="#">Portfolio</nuxt-link></li>
            <li><nuxt-link class="hover:text-[#f1e5a2]/80 transition" href="#">Pricing</nuxt-link></li>
          </ul>

          <u-button label="Get started" color="primary" size="xl" class="rounded-full">
            <template #trailing>
              <icon name="lucide:arrow-up-right" />
            </template>
          </u-button>
        </div>

        <!-- Mobile -->
        <button aria-label="menu-btn" type="button" class="menu-btn inline-block md:hidden active:scale-90 transition">
          <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 30 30" fill="#000">
            <path d="M 3 7 A 1.0001 1.0001 0 1 0 3 9 L 27 9 A 1.0001 1.0001 0 1 0 27 7 L 3 7 z M 3 14 A 1.0001 1.0001 0 1 0 3 16 L 27 16 A 1.0001 1.0001 0 1 0 27 14 L 3 14 z M 3 21 A 1.0001 1.0001 0 1 0 3 23 L 27 23 A 1.0001 1.0001 0 1 0 27 21 L 3 21 z"></path>
          </svg>
        </button>

        <div class="mobile-menu absolute top-17.5 left-0 w-full bg-white p-6 hidden md:hidden">
          <ul class="flex flex-col space-y-4 text-lg">
            <li><a href="#" class="text-sm">Home</a></li>
            <li><a href="#" class="text-sm">Services</a></li>
            <li><a href="#" class="text-sm">Portfolio</a></li>
            <li><a href="#" class="text-sm">Pricing</a></li>
          </ul>

          <button type="button" class="bg-white text-gray-600 border border-gray-300 mt-6 text-sm hover:bg-gray-50 active:scale-95 transition-all w-40 h-11 rounded-full">
            Get started
          </button>
        </div>
      </nav>

      <ul class="flex flex-col uppercase font-semibold p-10 absolute left-0 top-4/12">
        <li class="p-5 text-[#f1e5a2]">
          <nuxt-link class="hover:text-[#f1e5a2]/80 transition">Pin</nuxt-link>
        </li>
        <li class="p-5 text-[#f1e5a2]">
          <nuxt-link class="hover:text-[#f1e5a2]/80 transition">In</nuxt-link>
        </li>
        <li class="p-5 text-[#f1e5a2]">
          <nuxt-link class="hover:text-[#f1e5a2]/80 transition">X</nuxt-link>
        </li>
        <li class="p-5 text-[#f1e5a2]">
          <nuxt-link class="hover:text-[#f1e5a2]/80 transition">FB</nuxt-link>
        </li>
      </ul>

      <div class="absolute bottom-0 right-5 max-w-4xl text-right uppercase p-10 text-[#f1e5a2]">
        <motion :preset="VueUseMotions.SlideVisibleOnceTop" :duration="800">
          <p class="uppercase text-light leading-8">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam pariatur voluptate dolorem quaerat quisquam veritatis 
            amet molestias ullam totam quae.
          </p>
        </motion>

        <motion :preset="VueUseMotions.SlideVisibleOnceTop" :duration="400">
          <h1 class="font-bold text-9xl">
            Lucie Povaland
          </h1>
        </motion>
      </div>
    </div>

    <!-- Section 1 -->
    <div class="p-10 bg-transparent"> Some section</div>

    <!-- Section 2 -->
    <div id="unibody" class="px-10 py-20 bg-[#561417] space-y-30">
      <!-- Sub 1 -->
      <div class="grid grid-cols-2 gap-10">
        <motion :preset="VueUseMotions.FadeVisibleOnce" :duration="700">
          <div class="rounded-xl h-auto overflow-hidden">
            <nuxt-img src="back/infl1.jpg" class="aspect-square w-full object-cover" />
          </div>
        </motion>

        <div class="space-y-5">
          <h2 class="font-bold text-7xl uppercase text-[#f1e5a2]">
            Skills & capabilities
          </h2>
          <p class="text-[#f1e5a2] leading-8 uppercase font-light">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid sint quidem autem laudantium itaque asperiores harum natus minus ab voluptas nulla aut animi eligendi corporis in, doloremque iste rem numquam.
          </p>

          <div ref="percentageEl" class="mt-20 space-y-10">
            <div v-for="i in 3" :key="i" class="space-y-5 text-[#f1e5a2]">
              <div class="flex items-center justify-between">
                <p class="uppercase font-semibold">Some skill</p>
                <!-- <p class="uppercase font-semibold">56%</p> -->
                <p class="uppercase font-semibold">{{ animatedCount.toFixed(0) }}%</p>
              </div>
              <div class="flex gap-1">
                <div v-for="i in 38" :key="i" class="w-2 h-5 bg-[#f1e5a2]" />
                <div v-for="i in 38" :key="i" class="w-2 h-5 bg-[#f1e5a2]/20" />
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Sub 2 -->
      <div class="uppercase text-[#f1e5a2]">
        <div class="text-center max-w-3xl mx-auto space-y-5">
          <motion :preset="VueUseMotions.SlideVisibleOnceTop" :duration="600">
            <h2 class="font-bold text-7xl">
              My creative design process
            </h2>
          </motion>
          <p class="font-light leading-8">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quo, quia facilis repellat autem, at laudantium id quasi ex deleniti accusamus sequi quas cum iste minima aut provident. Officiis, eum nostrum.
          </p>
        </div>

        <div class="grid grid-cols-4 gap-5 mt-20">
          <div v-for="i in 4" :key="i" class="bg-[#f1e5a2]/10 p-10 rounded-xl">
            <div class="font-bold text-8xl w-full text-right opacity-20">
              0{{ i }}
            </div>

            <div class="mt-30">
              <h4 class="font-bold text-2xl">
                Title {{ i }}
              </h4>

              <div class="mt-3 text-[#f1e5a2]/50">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo cum iste qui, soluta laboriosam vero deleniti consequuntur autem natus
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Sub 3 -->
      <div class="grid grid-cols-12 gap-5 uppercase text-[#f1e5a2]">
        <div class="col-span-4">
          <div class="p-10 bg-[#f1e5a2]/10 rounded-xl">
            <div class="font-bold text-8xl w-full text-right opacity-20">
              2016
            </div>

            <div class="mt-20">
              <h4 class="font-bold text-2xl">
                The beginning
              </h4>

              <p class="mt-3 text-[#f1e5a2]/50">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo cum iste qui, soluta laboriosam vero deleniti consequuntur autem natus
              </p>
            </div>
          </div>
        </div>

        <div class="col-span-8">
          <div class="px-10">
            <h2 class="font-bold text-7xl">
              Built through experience
            </h2>

            <p class="mt-3 text-[#f1e5a2]/50">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo cum iste qui, soluta laboriosam vero deleniti consequuntur autem natus
            </p>
          </div>
        </div>

        <div class="col-span-5 col-start-2 text-[#561417]">
          <div class="p-10 bg-[#f1e5a2] rounded-xl">
            <div class="font-bold text-8xl w-full text-right opacity-20">
              2016
            </div>

            <div class="mt-20">
              <h4 class="font-bold text-2xl">
                Discovering figma
              </h4>

              <p class="mt-3 text-[#561417]/50">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo cum iste qui
              </p>
            </div>
          </div>
        </div>

        <div class="col-span-6">
          <div class="p-10 bg-[#f1e5a2]/10 rounded-xl">
            <div class="font-bold text-8xl w-full text-right opacity-20">
              2016
            </div>

            <div class="mt-20">
              <h4 class="font-bold text-2xl">
                The beginning
              </h4>

              <p class="mt-3 text-[#f1e5a2]/50">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo cum iste qui, soluta laboriosam vero deleniti consequuntur autem natus
              </p>
            </div>
          </div>
        </div>

        <div class="col-span-7 col-start-2">
          <div class="p-10 bg-[#f1e5a2]/10 rounded-xl">
            <div class="font-bold text-8xl w-full text-right opacity-20">
              2016
            </div>

            <div class="mt-20">
              <h4 class="font-bold text-2xl">
                Building with purpose
              </h4>

              <p class="mt-3 text-[#f1e5a2]/50">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Illo cum iste qui, soluta laboriosam vero deleniti consequuntur autem natus
              </p>
            </div>
          </div>
        </div>

        <div class="col-span-4 overflow-hidden rounded-xl">
          <nuxt-img src="/back/infl1.jpg" class="aspect-square object-cover" />
        </div>
      </div>

      <!-- Sub 4 -->
      <div class="grid grid-cols-12 gap-5 text-[#f1e5a2] w-full">
        <div class="col-span-5">
          <motion :preset="VueUseMotions.SlideVisibleOnceLeft" :duration="600">
            <h2 class="font-bold text-7xl uppercase">
              Skills & capabilities
            </h2>
 
          </motion>

          <u-button label="View all services" size="xl" class="rounded-full my-10">
            <template #trailing>
              <icon name="lucide:arrow-up-right" />
            </template>
          </u-button>
        </div>
        
        <div class="col-span-7">
          <div class="border-t border-b-2 border-[#f1e5a2]/20 py-10">
            <div class="flex items-center justify-between">
              <h4 class="text-2xl font-bold uppercase">
                Web design
              </h4>

              <div class="flex gap-1">
                <div v-for="i in 3" :key="i" class="bg-[#f1e5a2] w-2 h-2" />
                <div v-for="i in 2" :key="i" class="bg-[#f1e5a2]/50 w-2 h-2" />
              </div>
            </div>

            <p class="text-light text-sm uppercase leading-8 mt-5">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempora, velit. Totam molestiae accusamus, commodi tenetur repudiandae ab.
            </p>
          </div>

          <div class="border-t border-b-2 border-[#f1e5a2]/20 py-10">
            <div class="flex items-center justify-between">
              <h4 class="text-2xl font-bold uppercase">
                Web design
              </h4>

              <div class="flex gap-1">
                <div v-for="i in 3" :key="i" class="bg-[#f1e5a2] w-2 h-2" />
                <div v-for="i in 2" :key="i" class="bg-[#f1e5a2]/50 w-2 h-2" />
              </div>
            </div>

            <p class="text-light text-sm uppercase leading-8 mt-5">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempora, velit. Totam molestiae accusamus, commodi tenetur repudiandae ab.
            </p>

            <div class="grid grid-cols-3 auto-cols-min mt-5 gap-5 text-[#f1e5a2]">
              <nuxt-img src="/back/infl1.jpg" class="rounded-xl" alt="" />
              <nuxt-img src="/back/infl1.jpg" class="rounded-xl" alt="" />

              <ul class="space-y-2 flex flex-col justify-center">
                <li v-for="i in 5" :key="i" class="flex items-center gap-3">
                  <icon name="lucide:plus" />
                  Lorem ipsum dolor sit, amet
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Sub 5 -->
      <div class="grid gap-20 grid-cols-2">
        <div>
          <motion :preset="VueUseMotions.SlideVisibleOnceLeft" :duration="600">
            <h2 class="font-bold text-7xl uppercase text-[#f1e5a2]">
              Let's create something
            </h2>
          </motion>

          <p class="text-[#f1e5a2] leading-8 uppercase font-light mt-5">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Accusantium, tempora fuga repellendus 
            cum inventore itaque 
          </p>
        </div>
        
        <form class="p-10 rounded-xl bg-[#f1e5a2]/10 space-y-5">
          <div class="flex gap-5">
            <u-input size="xl" class="w-full" placeholder="Fullname" />
            <u-input size="xl" class="w-full" placeholder="Email address" />
          </div>

          <div class="flex gap-5">
            <u-input size="xl" class="w-full" placeholder="Project name" />
            <u-input size="xl" class="w-full" placeholder="Budget range" />
          </div>

          <u-textarea :style="{ resize: 'none' }" :rows="6" size="xl" class="w-full" placeholder="Project details" />
        </form>
      </div>
    </div>

    <!-- Footer -->
    <footer class="p-10 bg-transparent uppercase">
      <div class="p-10 text-[#f1e5a2] bg-[#561417]">
        <motion :preset="VueUseMotions.SlideVisibleOnceTop" :duration="600">
          <h2 class="text-7xl font-bold max-w-3xl mx-auto text-center">
            Let's bring ideas to life
          </h2>
        </motion>

        <div class="flex justify-center mt-10">
          <u-button size="xl" class="rounded-full">
            Contact me now
          </u-button>
        </div>

        <div class="max-w-7xl mx-auto grid grid-cols-1 lg:grid-cols-3 gap-8 md:gap-12 py-20">
          <div class="lg:col-span-3 grid grid-cols-2 md:grid-cols-3 gap-8 md:gap-12 lg:gap-28 items-center">
            <!-- Products -->
            <div v-for="i in 3" :key="i" class="text-center">
              <h3 class="font-medium mb-4 text-md text-[#f1e5a2]/20">
                Section {{ i }}
              </h3>

              <ul class="space-y-3 text-lg">
                <li><nuxt-link to="#" class="hover:text-[#f1e5a2]/80 font-semibold">Components</nuxt-link></li>
                <li><nuxt-link to="#" class="hover:text-[#f1e5a2]/80 font-semibold">Templates</nuxt-link></li>
                <li><nuxt-link to="#" class="hover:text-[#f1e5a2]/80 font-semibold">Icons</nuxt-link></li>
              </ul>
            </div>
          </div>
        </div>

        <div class="max-w-7xl mx-auto mt-12 pt-4 border-t border-[#f1e5a2]/20 text-[#f1e5a2] flex justify-between items-center">
          <p class="text-sm">© <nuxt-time :datetime="new Date()" year="numeric" /> <span class="font-bold">Gency 313</span> <span>All right reserved.</span></p>
          <div class="text-sm">
            <nuxt-link>Terms and conditions</nuxt-link> •
            <nuxt-link>Privacy policy</nuxt-link>
          </div>
        </div>
      </div>
    </footer>
  </section>
</template>

<script lang="ts" setup>
import { TransitionPresets } from '@vueuse/core'

// https://dribbble.com/shots/27787281-Personal-Portfolio-Website-Design

onMounted(() => {
  document.body.style.background = "#f1e5a2"
})

const count = ref(0)
const animatedCount = ref(0)

if (import.meta.client) {
  const _animatedCount = useTransition(count, {
    duration: 1500,
    transition: TransitionPresets.easeOutExpo,
  })
  syncRef(_animatedCount, animatedCount, { direction: 'ltr' })
}

const percentageRef = useTemplateRef('percentageEl')
const { isVisible } = useElementVisibility(percentageRef, {
  controls: true
})

watchEffect(() => {
  if (isVisible.value) {
    count.value = 56
  } else {
    count.value = 0
  }
})

onMounted(() => {
  // count.value = 56
})
</script>
