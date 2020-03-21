<template>
  <footer>
    <div class="container-fluid desktop_footer">
      <div class="row mt-2"></div>
      <div class="row mt-2">
        <div class="col-1"></div>
        <div class="col-2 mt-3">
          <div class="row">
            <i class="fab fa-whatsapp"></i>
          </div>
          <div class="row text-white">
            <p>
              Made in Medellín, Antioquia, Colombia
            </p>
          </div>
        </div>
        <div class="col-1"></div>
        <div class="col-2 text-white mt-5">
          <h3 class="text-white">Servicios</h3>
          <ul>
            <li>
              <nuxt-link
                :to="{
                  path: '/buscar' + '/inmueble' + '/arriendo' + '/centro',
                  query: {
                    latitud: 6.248443,
                    longitud: -75.554718,
                    precioMinimo: 500000,
                    precioMaximo: 2000000,
                    area: 0,
                    habitaciones: 1,
                    banos: 1,
                    pagina: 1
                  }
                }"
              >
                Comprar
              </nuxt-link>
            </li>
            <li>
              <nuxt-link
                :to="{
                  path: '/buscar' + '/inmueble' + '/venta' + '/centro',
                  query: {
                    latitud: 6.248443,
                    longitud: -75.554718,
                    precioMinimo: 500000,
                    area: 0,
                    habitaciones: 1,
                    banos: 1,
                    pagina: 1
                  }
                }"
              >
                Arrendar
              </nuxt-link>
            </li>
          </ul>
        </div>
        <div class="col-1"></div>
        <div class="col-2 iconoredes2 mt-5">
          <a
            href="https://es-la.facebook.com/arrendamientosnutibara/"
            target="_blank"
            rel="noopener noreferrer"
          >
            <i class="fab fa-whatsapp"></i>
          </a>
          <a
            href="https://www.instagram.com/arrendamientosnutibara/?hl=es-la"
            target="_blank"
            ><i class="fab fa-whatsapp"></i></a>
          <a href="mailto:info@anutibara.com?Subject=''" target="_blank"
            ><i class="fab fa-whatsapp"></i></a>
          <a
            href="https://wa.me/573117803657?text=Hola%2C%20estoy%20buscando%20un%20inmueble%20y%20me%20gustaria%20recibir%20asesoria%20para%20encontrarlo%2C%20me%20interesa..."
            target="_blank"
            ><i class="fab fa-whatsapp"></i></a>
        </div>
      </div>
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