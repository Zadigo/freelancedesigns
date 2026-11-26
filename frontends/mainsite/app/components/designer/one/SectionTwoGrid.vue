<template>
  <div class="p-20 rounded-xl text-[#0044AB]">
    <div class="grid grid-cols-2 gap-10">
      <div>
        <h5 class="text-lg uppercase font-bold">
          <slot name="title" />
        </h5>

        <slot name="secondary" />
      </div>

      <div>
        <slot />
      </div>
    </div>
  </div>
</template>
