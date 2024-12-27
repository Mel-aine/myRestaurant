<script setup>
import DefaultLayout from './components/layouts/DefaultLayout.vue';
import router from './router';

const isLogin = true;
</script>


  
<template>
  <template v-if="isLogin">
    <DefaultLayout>
      <RouterView />
    </DefaultLayout>
  </template>
  <template v-else>
    <DefaultLayout>
      <RouterView />
    </DefaultLayout>
  </template>
</template>




<style scoped>
/* Ajout de styles personnalisés si nécessaire */
</style>
