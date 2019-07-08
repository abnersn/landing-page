<template>
  <header class="Header">
    <figure class="Header-logo">
      <a href="/">
        <img src="../assets/logo.svg" alt="Logo buzzmonitor" />
      </a>
    </figure>
    <ul class="Header-social">
      <li>
        <a href="https://facebook.com" title="Facebook">
          <img
            class="glyph"
            src="../assets/social-icons/facebook.svg"
            alt="Nossa página no facebook"
          />
        </a>
      </li>
      <li>
        <a href="https://instagram.com" title="Instagram">
          <img class="glyph" src="../assets/social-icons/instagram.svg" alt="Nosso instagram" />
        </a>
      </li>
      <li>
        <a href="https://twitter.com" title="Twitter">
          <img class="glyph" src="../assets/social-icons/twitter.svg" alt="nosso perfil no twitter" />
        </a>
      </li>
      <li>
        <a href="https://youtube.com" title="Youtube">
          <img class="glyph" src="../assets/social-icons/youtube.svg" alt="Nosso canal no youtube" />
        </a>
      </li>
    </ul>
    <nav class="Header-nav">
      <a href="#conheca">Conheça</a>
      <a href="#e-books">E-Books</a>
      <a href="#planos">Planos</a>
      <a href="#clientes">Clientes</a>
      <a href="#blog">Blog</a>
      <a href="#use_gratis">Use Grátis</a>
    </nav>
  </header>
</template>

<style scoped lang="scss">
@import "../theme.scss";
$gutter: 0.5em;
$height: 3rem;
.Header {
  background: $background-color;
  position: sticky;
  height: $height;
  top: 0;
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
  & > * {
    margin: $gutter;
  }
}
.Header-logo {
  height: 100%;
  padding: 0.5rem 0;
  img {
    height: 100%;
  }
}
.Header-social {
  list-style-type: none;
  flex: 0 0 calc(4 * 2em);
  li {
    display: inline-block;
  }
  a {
    padding: $gutter;
  }
}
.Header-nav {
  text-transform: uppercase;
  margin-left: auto;
  display: flex;
  a {
    color: inherit;
    display: inline-block;
    white-space: nowrap;
    text-decoration: none;
    padding: $gutter;
  }
}
@media screen and (max-width: $bp-tablet) {
  .Header-nav {
    position: absolute;
    top: $height;
    left: 0;
    right: 0;
    padding: 0;
    margin: 0;
    width: 100%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background: $background-color;
  }
}
</style>

<script>
export default {
  name: "Header",
  props: ["fixed"]
};
</script>


