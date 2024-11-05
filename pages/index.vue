<template>
  <div class="bg-dotted flex min-h-screen flex-col items-center justify-center">
    <!-- <div class="flex"> -->
    <NuxtImg
      src="/images/headshot.jpg"
      sizes="100vw sm:50vw md:400px"
      class="mb-6 size-32 rounded-full sm:size-48" />

    <div class="container text-center ">
      <h2 class="text-4xl font-bold sm:text-6xl ">
        Phillip Hartin<span class="ml-2 text-base text-gray-500">PhD</span>
      </h2>
      <h1 class="mt-2 font-light sm:text-lg">
        Building digital products, services, and companies.
      </h1>
    </div>

    <footer
      class="fixed bottom-0 my-12 flex w-fit gap-8 rounded-full border border-black/[8%] bg-white px-6 py-3.5 font-mono text-sm font-light text-gray-500 shadow-sm">
      <NuxtLink
        v-for="link in links"
        :key="link.label"
        :to="link.to"
        class="hover:underline">{{ link.label }}</NuxtLink>
    </footer>
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
