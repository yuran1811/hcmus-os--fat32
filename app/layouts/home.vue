<template>
  <LayoutBlank :fixed="true">
    <div class="relative overflow-hidden px-6 lg:px-8">
      <DesignTopBlob />
      <DesignBottomBlob />

      <slot />
    </div>
  </LayoutBlank>
</template>
