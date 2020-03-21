<template>
  <footer>
    <div class="container-fluid desktop_footer">
      <div class="row justify-content-center copyright2 mt-4">
        <p class="text-white">© 2020 COVID-19</p>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  data() {
    return {}
  }
}
</script>
<style scoped>
li {
  margin-bottom: 8px;
}
.text-white {
  color: white;
}
h3 {
  margin-bottom: 1rem;
  font-weight: bolder;
  font-size: 1.4em;
}
ul {
  list-style: none;
  padding: 0;
}
footer {
  font-family: 'Helvetica';
  font-size: 1em;
  height: auto;
  line-height: 1.4rem;
  width: 100vw;
  position: relative;
  bottom: 0;
  background-color: #17a2b8;
  padding: 0px;
  margin: 0px;
}
li a {
  text-decoration-line: none;
}
a:link,
a:visited {
  color: white;
  text-decoration: none;
  cursor: pointer;
}

a:link:active,
a:visited:active {
  color: white;
}
.iconoredes img {
  margin-right: 0.8rem;
}
.iconoredes2 {
  display: inline-flex;
}
.iconoredes2 img {
  margin-right: 0.8rem;
}
.copyright {
  position: absolute;
  bottom: 0px;
  width: 100%;
}
.copyright2 p {
  margin-bottom: 0px;
}
.desktop_footer {
  display: none;
  height: 20rem;
}
</style>