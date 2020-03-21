<template>
  <div class="grid-container">
    <header class="header">
      <Header />
    </header>
    <main class="main">
      <nuxt />
    </main>
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  components: {
    Header
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

main {
  grid-area: 2 / 1 / 3 / 2;
  margin-top: 4.5rem;
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