<template>
  <div>
    <p>Hello World</p>
    <p v-once>My name is {{ myName }}</p>
    <p>My name is {{ myName }}</p>
    <p>Number: {{ randomNumber }}</p>
    <input v-model="randomNumber" />
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
      this.randomNumber = this.randomNumber++;
    },
  },
  mounted() {
    this.myName = "Jet Li";
  },
};
</script>

<style scoped></style>
