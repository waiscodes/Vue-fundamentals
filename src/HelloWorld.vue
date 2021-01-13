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
};
</script>

<style scoped></style>
