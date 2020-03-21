<template>
  <div class="grid-container">
    <header class="header">
      <Header />
    </header>
      <nuxt />
    <Footer class="footer" />
  </div>
</template>

<script>
import Header from '@/components/Header'
import Footer from '@/components/Footer'

export default {
  components: {
    Header,
    Footer
  },
  data() {
    return {}
  }
}
</script>

<style>
body,
html {
  overflow-x: hidden;
}
*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
.grid-container {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 70px fit-content auto;
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  min-height: 100vh;
}

header {
  grid-area: 1 / 1 / 2 / 2;
  height: fit-content;
}

footer {
  grid-area: 3 / 1 / 4 / 2;
}
@media (min-width: 320px) and (max-width: 768px) {
  main {
    margin-top: 1rem;
  }
}
</style>