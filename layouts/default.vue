<template>
  <div>
    <my-navbar />
    <nuxt />
  </div>
</template>

<script>
import MyNavbar from '@/components/MyNavbar.vue'

export default {
  components: {
    'my-navbar': MyNavbar
  }
}
</script>
