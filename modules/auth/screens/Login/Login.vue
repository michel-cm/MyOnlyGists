<script setup lang="ts">
import SocialForm from '../../components/SocialForm/SocialForm.vue';

const loading = ref(false);

const handleGithubLogin = async () => {
  loading.value = true;
  // @TODO call api
}

</script>

<template>
  <section class="w-full h-screen flex flex-col items-center justify-center gap-5 bg-gray-50">
    <Logo />
    <SocialForm :loading="loading" @wants-login-with-github="handleGithubLogin" />
  </section>
</template>