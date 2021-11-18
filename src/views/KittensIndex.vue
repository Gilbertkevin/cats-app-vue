<template>
  <div class="Kittens">
    <div v-for="kitten in kittens">
      <h1>{{ kitten.name }}</h1>
      <p>{{ kitten.breed }}</p>
      <p>{{ kitten.age }}</p>
    </div>
  </div>
</template>

<style></style>

<script>
import axios from 'axios';
  export default {
    data: function () {
      return {
        message: "See these Kittens",
        kittens: [],
      };
    },
    created: function () {
      this.indexKittens();
    },
    methods: {
      indexKittens: function () {
        console.log("see the kittens...")
        axios.get("/kittens").then((response) => {
          console.log(response.data);
          this.kittens = response.data;
        });
      },
    },
  };
</script>