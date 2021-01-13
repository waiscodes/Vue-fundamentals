<template>
  <div>
    <p>Hello World</p>
    <p v-once>My name is {{ myName }}</p>
    <p>My name is {{ myName }}</p>
    <input :value="randomNumber" />
    <button @click="changeNum">Change Number</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      myName: "Birm Wais",
      randomNumber: 5,
    };
  },
  methods: {
    helloWorld() {
      alert("Something");
    },
    changeNum() {
      this.randomNumber = 100;
    },
  },
  mounted() {
    this.myName = "Jet Li";
  },
};
</script>

<style scoped></style>
