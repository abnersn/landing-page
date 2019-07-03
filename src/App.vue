<template>
  <div>
    <Header />
    <main>
      <section id="conheca" class="test-section" />
      <section id="e-books" class="test-section" />
      <section id="planos" class="test-section" />
      <section id="clientes" class="test-section" />
      <section id="blog" class="test-section" />
      <section id="use-gratis" class="test-section" />
    </main>
  </div>
</template>

<script>
import Header from "./components/Header";
import "reset-css";

export default {
  name: "app",
  components: { Header }
};
</script>
<style lang="scss">
@import "theme";

body {
  font-size: 16px;
  background: palegoldenrod;
  font-family: $font-family;
  color: $text-color;
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
.test-section {
  height: 110vh;
}
</style>
