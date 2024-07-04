<script setup>
import { useSanityFetcher } from 'vue-sanity'

const posts = useSanityFetcher('*[_type=="post"]{title,"author": author->name}')?.data?.value
console.log(posts)
</script>

<template>
  <ul>
  {{ posts }}
  <li v-for="post in posts">
    {{ post["title"] }} - {{ post["author"] }}
  </li>
</ul>
</template>
