<template>
  <div class="overflow-hidden relative">
    <motion :preset="VueUseMotions.FadeVisibleOnce">
      <nuxt-img :src="src" :class="`hover:${rotation}`" class="w-full aspect-square object-cover object-center hover:scale-110 transition-all ease-in-out duration-200" />
    </motion>
    
    <div class="absolute top-0 right-0 w-full p-5 text-white">
      <div class="flex justify-between items-center">
        <motion :preset="VueUseMotions.SlideVisibleOnceLeft" :duration="700">
          <p class="font-semibold text-2xl">
            {{ title }}
          </p>
        </motion>
        
        <u-button variant="link" color="neutral">
          <icon name="lucide:arrow-up-right" size="40px" class="text-white" />
        </u-button>
        <!-- <motion :preset="VueUseMotions.SlideVisibleRight" :duration="700">
        </motion> -->
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import type { AllowedComponentProps } from 'vue'

defineProps<{
  src: string
  title: string
  rotation: AllowedComponentProps['class']
}>()
</script>
