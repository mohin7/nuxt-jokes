<template>
  <div>
    <AppHeader/>
    <nuxt />
  </div>
</template>



<script>
import AppHeader from "@/components/AppHeader.vue"
export default {
  components: {
    AppHeader
  }
}
</script>
<style>
@import url('../node_modules//bootstrap/dist/css/bootstrap.min');
</style>
