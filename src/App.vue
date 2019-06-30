<template>
  <Header />
</template>

<script>
import Header from "./components/Header";
import 'reset-css';

export default {
  name: "app",
  components: { Header }
};
</script>
<style>
body {
  font-size: 16px;
  font-family: Arial, Helvetica, sans-serif;
}
button {
  padding: 0;
  border: none;
  font: inherit;
  color: inherit;
  background-color: transparent;
  cursor: pointer;
}
.glyph {
  width: 1rem;
  height: 1rem;
}
* {
  box-sizing: border-box;
}
</style>
