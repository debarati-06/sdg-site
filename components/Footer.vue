<template>
  <footer class="p-4 bg-white rounded-lg shadow md:px-8 container mx-auto">
    <hr class="my-2 border-gray-200 sm:mx-auto  lg:my-4">
    <div class="flex flex-col md:flex-row items-center md:justify-around">
      <a href="https://copsiitbhu.co.in" target="_blank" rel="noreferrer" class="flex items-center mb-4 sm:mb-0 order-1">
        <nuxt-img src="/COPS-Logo.webp" width="80" height="80" alt="COPS Logo" loading="lazy">
          COPS Logo
        </nuxt-img>
      </a>
      <span class="block text-sm text-gray-500 text-center order-3 md:order-2 mt-4 md:mt-0">© {{ new Date().getFullYear() }} <a href="https://copsiitbhu.co.in" target="_blank" rel="noreferrer" class="hover:underline">COPS</a> SDG™. All Rights Reserved.
      </span>
      <ul class="flex flex-wrap items-center order-2 md:order-3">
        <li v-for="x in quicklinks" :key="x.url">
          <NuxtLink :to="x.url" class="px-2 text-gray-500 hover:underline-transparent hover:text-black md:mr-6" no-prefetch>{{ x.content }}</NuxtLink>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
export default defineComponent({
  name: 'Footer',
  data  () {
    return {
      quicklinks: [
        {
          url: '/portfolio',
          content: 'Team'
        },
        {
          url: '/aboutus',
          content: 'About'
        },
        {
          url: '/blog',
          content: 'Blog'
        },
        {
          url: '/contact',
          content: 'Contact'
        }
      ]
    }
  }
})
</script>

<style scoped>
.icon {
  color: rgba(0, 0, 0, 0.5);
  transition: 1s ease-in-out;
}
.icon:hover {
  transition: 0s ease-in-out;
  color: #0f0;
  text-shadow: 0 0 120px #0f0;
}
</style>
