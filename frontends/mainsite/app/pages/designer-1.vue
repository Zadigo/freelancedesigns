<template>
  <section id="site">
    <u-container>
      <section id="hero" class="text-[#0044AB]">
        <div class="grid grid-cols-3 grid-rows-2 w-full gap-1">
          <div class="border rounded-xl border-[#0044AB]/10 p-10">
            <h1 class="text-4xl">
              Shaping identities for those ready to rise above the noise
            </h1>

            <u-button label="Contact me" size="xl" variant="outline" class="rounded-full mt-5" />
          </div>
          
          <div class="border rounded-xl border-[#0044AB]/10 overflow-hidden">
            <nuxt-img src="/back/des1.jpg" class="w-full aspect-square object-cover" alt="" />
          </div>
          
          <div class="border rounded-xl border-[#0044AB]/10 p-10 flex">
            <div class="grid grid-cols-2 gap-5 content-center">
              <div class="flex flex-col justify-between">
                <p class="text-sm">
                  Creating Orrisé. A study in frangrance identity
                </p>

                <u-button label="See project" variant="link" color="primary">
                  <template #trailing>
                    <icon name="lucide:arrow-up-right" />
                  </template>
                </u-button>
              </div>
              <div>
                <nuxt-img src="/back/des1.jpg" class="w-full aspect-square object-cover rounded-xl" alt="" />
              </div>
            </div>
          </div>
          
          <div class="col-span-3 grid grid-cols-subgrid">
            <div class="border rounded-xl border-[#0044AB]/10 p-10">
              <ul class="list-disc list-outside">
                <li v-for="i in 4" :key="i" class="leading-8">
                  Some speciality {{ i }}
                </li>
              </ul>
            </div>
  
            <div class="border rounded-xl border-[#0044AB]/10 p-10" />
            
            <div class="border rounded-xl border-[#0044AB]/10 p-10">
              London, UK
            </div>
            
            <div class="border rounded-xl border-[#0044AB]/10 p-10">
              <nuxt-time :datetime="new Date()" time-style="short" time-zone="Europe/Paris" />
            </div>

            <div class="border rounded-xl border-[#0044AB]/10 p-10" />

            <div class="border rounded-xl border-[#0044AB]/10 p-10">
              Avaialable now
            </div>
            <!-- <div class="grid grid-cols-6">
            </div> -->
          </div>
        </div>
      </section>

      <section class="bg-white p-20 rounded-xl shadow-sm">
        <div class="grid grid-cols-2 gap-5 mb-10">
          <div>
            <h5 class="text-lg uppercase font-bold">
              Case studies
            </h5>
          </div>
          
          <div class="leading-8">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est deleniti repellat voluptates nam vero voluptatem sit assumenda asperiores! Nulla maiores, id provident rem earum dolores! Explicabo saepe fuga eius exercitationem.
          </div>
        </div>

        <div class="space-y-5">
          <div v-for="i in 3" :key="i" class="bg-[#0044AB] text-white rounded-xl p-20">
            <div class="grid grid-cols-2 gap-5 w-full">
              <div class="flex flex-col justify-between">
                <div class="space-y-5">
                  <div class="space-x-3">
                    <u-badge variant="soft" color="neutral" size="xl" label="2025" class="rounded-full" />
                    <u-badge variant="soft" color="neutral" size="xl" label="Branding" class="rounded-full" />
                  </div>
  
                  <h3 class="text-3xl text-semibold bg-[#0044AB]/10">
                    Crafting orrisé: An immense study in frangrance identity
                  </h3>
                </div>
  
                <u-button label="See project" variant="link" color="primary">
                  <template #trailing>
                    <icon name="lucide:arrow-up-right" />
                  </template>
                </u-button>
              </div>
  
              <div>
                <nuxt-img src="/back/des1.jpg" class="aspect-square object-cover w-full rounded-xl" />
              </div>
            </div>
          </div>
        </div>
      </section>

      <designer-one-section-two-grid>
        <template #title>
          About
        </template>

        <template #secondary>
          <ul class="list-disc leading-8">
            <li v-for="i in 3" key="i">
              Critical thinking {{ i }}
            </li>
          </ul>
        </template>

        <div class="text-4xl leading-8">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Est deleniti repellat voluptates nam vero voluptatem sit assumenda asperiores! Nulla maiores, id provident rem earum dolores! Explicabo saepe fuga eius exercitationem.
        </div>
      </designer-one-section-two-grid>
    </u-container>

    <div class="bg-[#0044AB] p-10 px-20">
      Brands
    </div>

    <designer-one-section-two-grid>
      <template #title>
        Statistics
      </template>

      <template #secondary>
        <p class="mt-10 leading-8">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta incidunt, accusamus consectetur aliquam, fugiat culpa veritatis iste possimus dignissimos minima nulla sint quos! Dolorum harum totam accusamus. Repellat, exercitationem deserunt.
        </p>
      </template>

      <div v-for="i in 4" :key="i" class="bg-[#0044AB] p-5 rounded-xl flex justify-between items-center not-last:mb-1 text-white">
        <span class="text-3xl font-bold">100</span>
        <span>Projects completed</span>
      </div>
    </designer-one-section-two-grid>

    <designer-one-section-two-grid class="bg-[#0044AB] text-white">
      <template #title>
        Testimonial
      </template>

      <template #secondary>
        <p class="mt-10 leading-8">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta incidunt, accusamus consectetur aliquam, fugiat culpa veritatis iste possimus dignissimos minima nulla sint quos! Dolorum harum totam accusamus. Repellat, exercitationem deserunt.
        </p>
      </template>

      <div>
        <div class="flex justify-between">
          <nuxt-img src="/back/des1.jpg" class="w-20 h-20 rounded-xl" />
        </div>

        <p class="text-4xl font-light leading-12 mt-10">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt id voluptatibus voluptatum! 
          A suscipit fugiat possimus praesentium vitae! Eos illum sint harum necessitatibus distinctio explicabo optio, 
          quo voluptatem ab molestiae.
        </p>

        <p class="font-light font-sm my-10">
          Michael Thomposon, Marketing Director
        </p>

        <div class="flex gap-2">
          <u-button variant="outline" color="primary" icon="lucide:arrow-left" />
          <u-button variant="outline" color="primary" icon="lucide:arrow-right" />
        </div>
      </div>
    </designer-one-section-two-grid>

    <designer-one-section-two-grid class="text-[#0044AB]">
      <template #title>
        Services
      </template>

      <template #secondary>
        <p class="mt-10 leading-8">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta incidunt, accusamus consectetur aliquam, fugiat culpa veritatis iste possimus dignissimos minima nulla sint quos! Dolorum harum totam accusamus. Repellat, exercitationem deserunt.
        </p>
      </template>

      <div class="space-y-2">
        <div v-for="i in 2" :key="i" class="border rounded-xl flex justify-between items-center p-8">
          <span>00-1</span>
          <span class="font-bold text-2xl">Web design</span>
        </div>

        <div class="border rounded-xl flex justify-between items-center p-8 gap-10">
          <div class="flex flex-col justify-around">
            <span>00-3</span>
            <p class="font-bold text-2xl">
              Brand Identity Design
            </p>

            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Adipisci, quo dolorem? Ipsum obcaecati praesentium
            </p>
          </div>

          <nuxt-img src="/back/des1.jpg" class="aspect-square object-cover w-60 rounded-xl" alt="" />
        </div>
      </div>
    </designer-one-section-two-grid>
  </section>
</template>

<script setup lang="ts">
// https://dribbble.com/shots/26840259-James-Parker-Portfolio-Website-UI-UX-Design
// #0044AB
// #F4F3EF

onMounted(() => {
  document.body.style.backgroundColor = '#F4F3EF'
})
</script>
