<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import { useSanityFetcher } from 'vue-sanity'

const { data: title } = useSanityFetcher('*[_type == "post"][0].title')

</script>

<template>
  <main>
    <h2>{{ title }}</h2>
    <TheWelcome />
  </main>
</template>
