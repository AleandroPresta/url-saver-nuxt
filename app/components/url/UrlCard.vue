<script setup lang="ts">
import type {Url} from "~/domain/url.ts";
import CardDropdown from "~/components/url/CardDropdown.vue";

const props = defineProps<{ url: Url }>();
</script>

<template>
  <div
      class="card card-dash bg-base-100 mx-auto sm:mx-0 w-85 sm:w-96 shadow-xs hover:shadow-sm transition-shadow duration-75 ease-out">
    <div class="card-body">
      <div class="card-title">
        <p class="text-lg">{{ props.url.name }}</p>
        <CardDropdown :urlId="props.url.id"></CardDropdown>
      </div>
      <p>{{ props.url.description }}</p>
      <div class="card-actions justify-end">
        <a :href="props.url.value" class="btn btn-primary">Visit</a>
      </div>
    </div>
  </div>
</template>
