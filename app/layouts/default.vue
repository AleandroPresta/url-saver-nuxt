<script setup lang="ts">
import AppHeader from "~/components/AppHeader.vue";
import AppFooter from "~/components/AppFooter.vue";
</script>

<template>
  <div class="min-h-screen flex flex-col bg-base-200">
    <AppHeader/>
    <main class="flex-1 sm:px-4 md:px-8 lg:px-16 xl:px-32">
      <slot/>
    </main>
    <AppFooter/>
  </div>
</template>