<template>
  <div id="product">
    <article v-for="(movie, idx) in items" :key="idx">
      <img
        v-bind:src="'https://image.tmdb.org/t/p/w500' + movie.poster_path"
        width="100"
        height="100"
        alt
      />
      <h1>{{movie.title}}</h1>
      <Card title="test" />
    </article>
  </div>
</template>

<script>
import axios from "axios";
import Card from "./components/Card.vue";

export default {
  name: "Product",
  components: [Card],
  data() {
    return {
      items: []
    };
  },
  methods: {
    getProduct: async function() {
      let response = await axios.get(
        "https://api.themoviedb.org/3/movie/upcoming?api_key=a64533e7ece6c72731da47c9c8bc691f&language=ko-KR&page=1"
      );
      this.items = response.data.results;
    }
  },
  created() {
    this.getProduct();
  }
};
</script>

<style>
</style>