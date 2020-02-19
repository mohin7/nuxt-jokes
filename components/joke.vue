<template>
  <div>
    <p><nuxt-link :to="{path: '/jokes/'+id}">{{joke}}</nuxt-link></p>
  </div>
</template>

<script>
  export default {
    name: "joke",
    props: ['joke', 'id']
  }
</script>

<style scoped>
p{
  border: 1px solid #ddd;
  padding: 15px 10px;
}
</style>