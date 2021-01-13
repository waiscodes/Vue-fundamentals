<template>
  <div>
    <p>Hello World</p>
    <p v-once>My name is {{ myName }}</p>
    <p>My name is {{ myName }}</p>
    <p v-html="rawHTML"></p>
    <p>raw HTML: {{ rawHTML }}</p>
    <!-- Be careful with this method. Suspetible to cross site scripting -->
  </div>
</template>

<script>
export default {
  data() {
    // Data is a method that contains all the data that goes on the template
    return {
      myName: "Birm Wais",
      rawHTML: "<strong>raw HTML</strong>",
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
    this.myName = "Jet Li";
  },
};
</script>

<style scoped></style>
