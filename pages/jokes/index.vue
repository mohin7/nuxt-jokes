<template>
  <div>
    <div class="container">
      <Joke
      v-for="joke in jokes"
      :key="joke.id"
      :id="joke.id"
      :joke="joke.joke"
    />
    </div>
  </div>
</template>

<script>
import Joke from "@/components/joke";
import axios from "axios";
export default {
  components: {
    Joke
  },
  data() {
    return {
      jokes: []
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };
    try {
      const res = await axios.get("https://icanhazdadjoke.com/search", config);
      this.jokes = res.data.results;
    } catch (error) {
      console.log(error);
    }
  }
};
</script>

<style lang="scss" scoped></style>
