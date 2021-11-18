<template>
  <div class="kittenscreate">
    <h1>{{ message }}</h1>
  </div>
</template>

<style></style>

<script>
  export default {
    data: function () {
      return {
        message: "Add a Kitten!",
        newKitten: [],
      };
    },
    created: function () {},
    methods: {
      createKitten: function () {
        console.log("Let's add a cat!")
      }
    },
  };
</script>