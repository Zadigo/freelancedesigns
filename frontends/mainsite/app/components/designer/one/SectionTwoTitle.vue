<template>
  <section class="bg-white p-20 rounded-xl shadow-sm">
    <div class="grid grid-cols-2 gap-5 mb-10">
      <div>
        <h5 class="text-lg uppercase font-bold">
          <slot name="title" />
        </h5>
      </div>

      <div class="leading-8">
        <slot name="description" />
      </div>
    </div>

    <div class="space-y-5">
      <slot />
    </div>
  </section>
</template>
