<template>
  <div>
    <p>{{joke}}</p>
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