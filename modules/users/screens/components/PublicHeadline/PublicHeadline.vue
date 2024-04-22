<script setup lang="ts">

const props = withDefaults (
  defineProps<{
    name: string,
    avatarUrl: string,
    bio?: string,
    city?: string,
    state?: string
  }>(),
 {
  name: 'Michel Corrêa',
  avatarUrl: 'https://avatars.githubusercontent.com/u/58608300?v=4',
  bio: 'Programador Frontend',
  city: 'Poço Fundo',
  state: 'MG'
  }
)
</script>

<template>
  <div class="w-full flex flex-col justify-center items-center gap2">
    <div class="w-24 md:w-32 rounded-full overflow-hidden">
      <img :src="props.avatarUrl" alt="foto do usuário" class="w-full">
    </div>
    <h1 class="font-[Inter] text-gray-700 text-center font-bold text-2xl md:text-3xl">{{ props.name }}</h1>
    <p class="font-[Inter] text-gray-700 text-center font-regular md:text-lg" v-if="props.bio">{{ props.bio }}</p>
    <p class="font-[Inter] text-gray-500 font-regular text-sm md:text-base" v-if="props.bio && props.state">
    <i class="pi pi-map-marker"></i>
    {{ props.city }}, {{ props.state }}
    </p>
  </div>
</template>