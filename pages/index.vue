<template>
  <div>
    <Home></Home>
  </div>
</template>

<script>
import Home from '~/components/Home.vue'

export default {
  components: {
    Home
  },
  head() {
    return {
      title: 'Home',
      meta: [
        { hid: 'Home Page', name: 'Home', content: 'Nuxt.js Home Page'}
      ]
    }
  }
}
</script>