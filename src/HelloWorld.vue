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
  beforeCreate() {
    // this is called as soon as main.js mounts as the first method
    console.log("beforeCreate was called");
  },
  created() {
    // this gets called as soon as the template injections are done
    console.log("created was called");
  },
  beforeMount() {
    // This is called when the component is about to be mounted
    console.log("beforeMount was called");
  },
  mounted() {
    // This changes after the page is mounted.
    console.log("mounted was called");
    this.myName = "Bruce Lee"; // Name is first Birm Wais and then Bruce Lee
  },
  beforeUnmount() {},
  unmounted() {},
};
</script>

<style scoped></style>
