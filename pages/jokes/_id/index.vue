<template>
  <div class="container">
     <nuxt-link tag="button" class="btn btn-primary" to="/jokes">Back to joke</nuxt-link>
    <h3>{{ joke }}</h3>
    <p>Joke ID: <strong>{{this.$route.params.id}}</strong></p>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      joke: ""
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get(
        `https://icanhazdadjoke.com/j/${this.$route.params.id}`,
        config
      );
      this.joke = res.data.joke;
    } catch (error) {
      console.log(error);
    }
  }
};
</script>

<style lang="scss" scoped></style>
