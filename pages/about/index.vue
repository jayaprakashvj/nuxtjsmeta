<template>
<div class="text-center ">
  <nuxt-link to="/">home</nuxt-link>
  <nuxt-link to="about">about</nuxt-link>
</div>
  
</template>

<script>
export default {
    async asyncData ({ query, store }) {
       let pageinfo ={
           title:'about page dynamic',
           discription:'about page discription',
           ogImage:'http://wpr.intertoons.net/centrealadmin/assets/images/uploads/productimages/Dabur-Chyawanprash-2Ximmunity-500G-Centreal-Bazaar-Supermarket-in-Kerala.jpg'
       }

         return {
         pageinfo
      }
    },
    head() {
      return {
        title: this.pageinfo.title,
        meta: [
          {
            hid: 'description',
            name: 'description',
            content: this.pageinfo.discription
          },
          {
                hid: 'og:title',
                name: 'og:title',
                content: this.pageinfo.title,
            },
            {
                hid: 'og:image',
                property: 'og:image',
                content: this.pageinfo.ogImage,
            },
            {
                hid: 'og:description',
                property: 'og:description',
                content: this.pageinfo.description,
            },
            
        ]
      }
    }
}
</script>
