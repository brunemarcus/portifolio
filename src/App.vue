<template>
  <v-app>
    <v-main>
      <Navbar></Navbar>
      <v-container fluid>
        <h3 class="mb-3 text-uppercase" style="color:#585858;">
          Valores e Compromisso
        </h3>
        <Sobre></Sobre>
        <h3 class="mb-3 text-uppercase" style="color:#585858;">
          Tecnologias e Habilidades
        </h3>
        <Habilidades></Habilidades>
        <h3 class="mb-3 mt-3 text-uppercase" style="color:#585858;">
          Portifólio
        </h3>
        <Portifolio></Portifolio>
      </v-container>
      <Footer></Footer>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from './components/Navbar';
import Sobre from './components/Sobre'
import Habilidades from './components/Habilidades';
import Portifolio from './components/Portifolio';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Navbar,
    Sobre,
    Habilidades,
    Portifolio,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
