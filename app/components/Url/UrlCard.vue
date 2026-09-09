<script setup lang="ts">
import type {Url} from "~/domain/url.ts";

const props = defineProps<{url: Url}>();
</script>

<template>
  <div class="card card-dash bg-base-100 mx-auto sm:mx-0 w-85 sm:w-96 shadow-xs hover:shadow-sm transition-shadow duration-75 ease-out">
    <div class="card-body">
      <h2 class="card-title">{{ props.url.name }}</h2>
      <p>{{ props.url.description }}</p>
      <div class="card-actions justify-end">
        <a :href="props.url.value" class="btn btn-primary">Visit</a>
      </div>
    </div>
  </div>
</template>
