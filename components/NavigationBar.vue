<template>
<ul class="flex">
  <li class="mr-6">
    <nuxt-link class="text-blue-500 hover:text-blue-800" to="/blog">Blog</nuxt-link>
  </li>
  <li class="mr-6">
    <nuxt-link class="text-blue-500 hover:text-blue-800"  to="/">Projects</nuxt-link>
  </li>
  <li class="mr-6">
    <nuxt-link class="text-blue-500 hover:text-blue-800" to="/">About</nuxt-link>
  </li>
</ul>  
</template>

<script>
export default {
    name: 'NavigationBar'

}
</script>

<style>

</style>