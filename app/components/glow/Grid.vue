<script setup lang="ts">
const features = [
  {
    title: 'Lightning Fast',
    description: 'Optimized performance for the best user experience',
    color: '#3B82F6',
    fgClass: 'text-blue-500',
    bgClass: 'bg-blue-500/20',
    icon: 'M13 10V3L4 14h7v7l9-11h-7z',
  },
  {
    title: 'Secure',
    description: 'Security for your peace of mind',
    color: '#10B981',
    fgClass: 'text-green-500',
    bgClass: 'bg-green-500/20',
    icon: 'M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z',
  },
  {
    title: 'Reliable',
    description: '99.9% uptime guarantee for your business',
    color: '#F59E0B',
    fgClass: 'text-yellow-500',
    bgClass: 'bg-yellow-500/20',
    icon: 'M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15',
  },
];
</script>

<template>
  <GlowCapture :size="250">
    <slot />

    <div
      class="relative grid w-full grid-cols-1 gap-6 px-4 pt-20 pb-52 sm:px-8 md:grid-cols-2 md:px-20 lg:grid-cols-3"
    >
      <GlowElement
        v-for="feature in features"
        :key="feature.title"
        :color="feature.color"
        class="group"
      >
        <div
          class="glow:border-glow group-hover:glow:bg-glow/[.12] h-full rounded-xl border-2 border-transparent p-6 ring-1 ring-gray-800 transition"
        >
          <div
            :class="`${feature.bgClass} flex-center mb-4 size-12 rounded-lg`"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              :class="`${feature.fgClass} size-6`"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                :d="feature.icon"
              />
            </svg>
          </div>

          <h3 class="glow:text-glow mb-2 text-xl font-bold text-gray-200">
            {{ feature.title }}
          </h3>
          <p class="glow:text-glow/80 text-gray-400">
            {{ feature.description }}
          </p>
        </div>
      </GlowElement>
    </div>
  </GlowCapture>
</template>
