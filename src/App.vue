<template>
  <div>
    <Header />
    <main>
      <section id="conheca" class="test-section">
        <h2>Conheça o Buzzmonitor</h2>
      </section>
      <section id="e-books" class="test-section">
        <h2>E-books</h2>
      </section>
      <section id="planos" class="test-section">
        <h2>Planos</h2>
      </section>
      <section id="clientes" class="test-section">
        <h2>Clientes</h2>
      </section>
      <section id="blog" class="test-section"></section>
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
  background: linear-gradient(red, orange, yellow, limegreen, blue, purple);
  font-family: $font-family;
  color: $text-color;
  scroll-behavior: smooth;
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
  padding-top: 4rem;
  margin-top: -4rem;
  height: 110vh;
}
@media screen and (max-width: 869px) {
  .test-section {
    padding-top: 6rem;
    margin-top: -6rem;
  }
}
</style>
