<script setup lang="ts">

const urls = ref([
  {
    id: 'some_id',
    name: 'facebook',
    description: 'Facebook',
    value: 'https://www.facebook.com',
  }
]);

</script>

<template>
  <div class="mt-4 flex flex-col flex-wrap">
    <UrlCard v-for="url in urls" :key="url.id" :url="url"></UrlCard>
  </div>
</template>