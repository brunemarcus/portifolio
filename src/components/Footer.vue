<template>
    <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="item in social"
          :href="`${item.link}`"
          :key="item.icon"
          class="mx-4 white--text"
          target="_blank"
          icon
        >
          <v-icon size="24px">
            {{ item.icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Sou Desenvolvedor Web FullStack há aproximadamente 4 anos, estou sempre em busca de aprimorar meus conhecimentos e crescer como profissional sempre gosto de desafios e acredito ser a melhor forma de aprender mais. Entusiasta do mundo Crypto, DEFI e Metaverso e pretendo contribuir mais com o desenvolvimento dessas tecnologias nos próximos anos. Tenho metas claras e objetivas e busco pessoas e empresas que possam somar com meu desenvolvimento como profissional. Caso tenha se interessado no meu perfil e acredite que tenha um match com a vaga ou projeto, fique à vontade para entrar em contado através das minhas redes sociais e fazer sua proposta. 
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — Developed by <strong>Marcus Brune</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
    export default {
        data() {
            return {
               social: 
                [
                  {
                    icon: 'mdi-github',
                    link: 'https://github.com/brunemarcus'
                  },
                  {
                    icon: 'mdi-linkedin',
                    link: 'https://www.linkedin.com/in/marcus-vinicius-brune-205bb8124/'
                  },
                  {
                    icon: 'mdi-instagram',
                    link: 'https://www.instagram.com/brunemarcus/'
                  }
                ],
            }
        }
    }
</script>