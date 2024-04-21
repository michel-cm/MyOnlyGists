<script setup lang="ts">
import Logo from '@/components/Logo/Logo.vue'

const emit = defineEmits<{
  (e: 'wants-be-creator'): void
}>()

</script>

<template>
  <header class="w-full shadow">
    <nav class="bg-white px-4 lg:px-6 py-2">
      <div class="flex justify-center md:justify-between items-center mx-auto max-w-screen-xl">
        <div class="flex items-center">
          <nuxt-link to="/">
            <Logo />
          </nuxt-link>
        </div>
        
        <div class="hiddern md:flex items-center">
          <Button
             @click="emit('wants-be-creator')"        
            label="Continuar como creator"
            icon-pos="right"
            icon="pi pi-arrow-right"
          />
        </div>
      </div>
    </nav>
  </header>
</template>