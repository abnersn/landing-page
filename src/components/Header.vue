<template>
  <header class="Header">
    <figure class="Header-logo">
      <a href="/">
        <img src="../assets/logo.svg" alt="Logo buzzmonitor" />
      </a>
    </figure>
    <ul class="Header-social">
      <li>
        <a href="https://facebook.com">
          <img
            class="glyph"
            src="../assets/social-icons/facebook.svg"
            alt="Nossa página no facebook"
          />
        </a>
      </li>
      <li>
        <a href="https://instagram.com">
          <img class="glyph" src="../assets/social-icons/instagram.svg" alt="Nosso instagram" />
        </a>
      </li>
      <li>
        <a href="https://twitter.com">
          <img class="glyph" src="../assets/social-icons/twitter.svg" alt="nosso perfil no twitter" />
        </a>
      </li>
      <li>
        <a href="https://youtube.com">
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
    <button type="button" class="Header-login">
      <img class="glyph" src="../assets/glyphs/login.svg" alt="Entre agora" />
    </button>
  </header>
</template>

<style scoped lang="scss">
.Header {
  display: grid;
  grid-template-columns: 14rem auto 1fr 2rem;
  grid-template-areas: "logo social nav login";
  grid-gap: 1rem;
  width: 100%;
  height: 4rem;
  align-items: center;
}
.Header-logo {
  grid-area: logo;
  img {
    width: 14rem;
  }
}
.Header-social {
  grid-area: social;
  flex: calc(4 * 2rem);
  list-style-type: none;
  li {
    display: inline-block;
  }
  a {
    padding: 0.5rem;
  }
}
.Header-nav {
  grid-area: nav;
  justify-self: right;
  text-transform: uppercase;
  a {
    text-decoration: none;
    padding: 0.5rem;
  }
}
.Header-login {
  grid-area: login;
  padding: 0.5rem;
}
@media screen and (max-width: 1080px) {
  .Header {
    grid-template-columns: 1fr 1fr;
    grid-template-areas:
      "logo social"
      "nav login";
  }
}
</style>

<script>
export default {
  name: "Header"
};
</script>


