<template>
  <header>
    <h1>
      {{ title }}
    </h1>
  </header>
</template>

<script>
export default {
  data() {
    return {
      title: "View practice using click events and v-for",
    };
  },
};
</script>

<style scoped>
header {
  background: rgb(56, 247, 56);
  padding: 10px;
}
h1 {
  color: #222;
  text-align: center;
}
</style>
