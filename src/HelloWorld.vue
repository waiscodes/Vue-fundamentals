<template>
  <div>
    <h2>Speed Typer</h2>
    <p>
      <span v-for="keyword in keywords" :key="keyword"
        >{{ keyword }}&nbsp;</span
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
export default {
  data() {
    return {
      keywords: [
        "hockey",
        "soccer",
        "basketball",
        "baseball",
        "something",
        "random",
        "okay",
        "zebra",
      ],
    };
  },
  methods: {},
};
</script>

<style scoped></style>
