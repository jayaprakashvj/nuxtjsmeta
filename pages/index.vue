<template>
<div class="text-center ">
  <nuxt-link to="/">home</nuxt-link>
  <nuxt-link to="about">about</nuxt-link>
</div>
  
</template>

<script>
export default {
   layout: 'default',
   head() {
      return {
        title: 'home page',
        meta: [
          {
            hid: 'description',
            name: 'home page discription',
            content: 'Home page description'
          }
        ]
      }
    }
}
</script>
