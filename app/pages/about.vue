<script setup lang="ts">
definePageMeta({
  name: 'About',
  icon: 'lucide:info',
  description: 'About',
  category: 'system',
});
</script>

<template>
  <LayoutDefault>
    <section class="space-y-12 pb-24">
      <GlowGrid>
        <div class="flex-center-col mx-auto mb-8 gap-6">
          <h2 class="text-center font-bold text-2xl sm:text-4xl md:text-6xl">
            yupartify
          </h2>
          <p class="mx-auto text-center text-base sm:text-lg md:text-xl">
            A robust, powerful disk manager
          </p>
        </div>
      </GlowGrid>
    </section>

    <Dock />
  </LayoutDefault>
</template>
