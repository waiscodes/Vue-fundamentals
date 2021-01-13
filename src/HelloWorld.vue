<template>
  <div>
    <p>Hello World</p>
    <p>My name is {{ myName }}</p>
  </div>
</template>

<script>
export default {
  data() {
    // Data is a method that contains all the data that goes on the template
    return {
      myName: "Birm Wais",
    };
  },
  methods: {
    // This is just a regular object not a function like methods
    // You define your methods inside this object
    helloWorld() {
      alert("Something");
    },
  },
  mounted() {
    this.helloWorld();
  },
};
</script>

<style scoped></style>
