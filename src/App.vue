<script setup>
import { useSanityClient } from 'vue-sanity'
import { RouterView } from 'vue-router';
import Filters from "./components/Filters.vue";

useSanityClient({
    projectId: '4cxom23e',
    dataset: 'production',
    useCdn: true,
})


</script>

<template>
    <header>
      <nav class="flex flex-wrap justify-between items-center md:flex-nowrap md:gap-10">
        <RouterLink to="/" class="font-cursive text-6xl no-underline text-nowrap">Where's the Cake?</RouterLink>
        <Filters />
      </nav>
    </header>
    <main>
      <RouterView /> <!-- looks up the slug in router.js and inserts the respective view -->
    </main>
</template>
<style>
#app {
  @apply container px-8 mx-auto xl:px-5  max-w-screen-lg py-5 lg:py-8;
}
</style>