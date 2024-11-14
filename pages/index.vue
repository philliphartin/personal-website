<template>
  <div class="bg-dotted flex min-h-screen flex-col items-center justify-center">
    <NuxtImg
      src="/images/phillip.jpg"
      sizes="100vw sm:50vw md:400px"
      class="mb-6 size-32 rounded-full sm:size-48" />

    <div class="container text-center ">
      <h2 class="text-5xl font-bold">
        Phillip Hartin<span class="ml-2 text-base text-gray-500">PhD</span>
      </h2>
    </div>

    <div
      class="my-4 flex w-fit gap-8 font-mono text-sm font-light text-gray-500">
      <NuxtLink
        v-for="link in links"
        :key="link.label"
        :to="link.to"
        class="hover:text-gray-900 hover:underline">{{ link.label }}</NuxtLink>
    </div>
  </div>
</template>

<script setup lang="ts">
const links = ref([
  {
    label: 'GitHub',
    to: 'https://github.com/philliphartin',
  },
  {
    label: 'LinkedIn',
    to: 'https://www.linkedin.com/in/philliphartin/',
  },
  {
    label: 'Airlume',
    to: 'https://airlume.cloud',
  },
  {
    label: 'Laravel',
    to: 'https://laravel.com',
  },
])
</script>
