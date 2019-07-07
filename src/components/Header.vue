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
.Header {
  background: $background-color;
  position: sticky;
  top: 0;
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
  & > * {
    margin: $gutter;
  }
}
.Header::after,
.Header::before {
  content: "";
  width: 1rem;
  height: 2rem;
  position: absolute;
  bottom: 0;
}
.Header::after {
  right: 0;
  background: linear-gradient(
    to right,
    transparent,
    $background-color,
    $background-color
  );
}
.Header::before {
  left: 0;
  background: linear-gradient(
    to left,
    transparent,
    $background-color,
    $background-color
  );
}
.Header-logo {
  img {
    height: 2em;
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
@media screen and (max-width: 920px) {
  .Header {
    flex-wrap: wrap;
    justify-content: flex-start;
  }
  .Header-social {
    margin-left: auto;
  }
  .Header-nav {
    white-space: nowrap;
    overflow-x: auto;
    scrollbar-width: none;
    text-align: center;
    margin: auto;
  }
  .Header-nav > *:first-child {
    padding-left: 1rem;
  }
  .Header-nav > *:last-child {
    padding-right: 1rem;
  }
  .Header-nav::-webkit-scrollbar {
    background: transparent;
    width: 0;
    height: 0;
  }
}
@media screen and (max-width: 380px) {
  .Header {
    justify-content: center;
    font-size: 0.8rem;
  }
  .Header-social {
    display: none;
  }
}
</style>

<script>
export default {
  name: "Header",
  props: ["fixed"]
};
</script>


