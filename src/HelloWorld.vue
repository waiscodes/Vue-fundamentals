<template>
  <div>
    <h2>My Favourite Languages</h2>
    <p>{{ keywords.join(" | ") }}</p>
    <input :value="inputValue" @keyup.space="processInput($event)" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      index: 0,
      keywords: [],
      inputValue: "",
    };
  },
  methods: {
    processInput(e) {
      const value = event.target.value;
      this.keywords[this.index] = value;
      this.inputValue = "";
      this.index++;
      console.log(e);
    },
  },
};
</script>

<style scoped></style>
