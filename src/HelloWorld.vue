<template>
  <div>
    <h2>Speed Typer</h2>
    <p>
      <span v-for="keyword in keywords" :key="keyword"
        >{{ keyword.text }}&nbsp;</span
      >
      <input
        type="text"
        :value="inputValue"
        @keyup.space="processInput($event)"
      />
    </p>
  </div>
</template>

<script>
const defaultKeywords = [
  "hockey",
  "soccer",
  "basketball",
  "baseball",
  "something",
  "random",
  "okay",
  "zebra",
].map((keyword) => {
  return {
    text: keyword,
    correct: false,
    wrong: false,
    pending: true,
  };
});

export default {
  data() {
    return {
      inputValue: "",
      index: "",
      keywords: defaultKeywords,
    };
  },
  methods: {
    processInput(e) {
      const value = e.target.value;

      if (value === "") {
        return;
      }

      if (this.keywords[this.index] === value) {
        // correct answer
      } else {
        // wrong answer
      }

      this.inputValue = "";
      this.index++;
    },
  },
};
</script>

<style scoped></style>
