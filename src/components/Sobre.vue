<template>
    
    <div>
       
        <v-row no-gutters>
            <v-col 
                v-for="item in about" 
                :key="item.title"
                cols="12"
                sm="4"
            > 
            <v-hover
                v-slot="{ hover }"
                open-delay="200"
            >
                <v-card 
                    :elevation="hover ? 16 : 2"
                    :class="{ 'on-hover': hover }"
                    class="mb-4" 
                    max-width="400" 
                    height="350px">
                    <v-img
                        class="white--text align-end"
                        height="200px"
                        :src="require(`@/assets/images/${item.profile}`)" 
                    >
                        <v-card-title v-text="item.title"></v-card-title>
                    </v-img>
                    <v-card-subtitle class="pb-0" v-text="item.subtitle"></v-card-subtitle>
                    <v-card-text class="text--primary">
                        <div v-text="item.overview"></div>
                    </v-card-text>

                </v-card>
            </v-hover>
            </v-col>
        </v-row>

    </div>

</template>

<style lang="sass" scoped>
.v-card.on-hover.theme--dark
  background-color: rgba(#FFF, 0.8)
  >.v-card__text
    color: #000
</style>

<script>
    export default {
        data() {
            return {
                about: [
                    {
                        title: 'Comprometimento',
                        subtitle: 'Compromentimento com a satisfação do cliente',
                        overview: 'A Satisfação do cliente com o produto final é uma peça chave e fundamental para estabeler uma relação duradoura.',
                        profile: 'valores.jpg'
                    },
                    {
                        title: 'Responsabilidade',
                        subtitle: 'Foco em qualidade e prazos',
                        overview: 'Responsabilidade com a entrega, qualidade do produto do cliente.',
                        profile: 'responsabilidade.jpg'
                    },
                    {
                        title: 'Qualidade',
                        subtitle: 'Aplicações seguras e qualificadas',
                        overview: 'É Fundamental o foco na qualidade da aplicação do cliente soluções eficientes, segurança e escalabilidade.',
                        profile: 'qualidade.jpg'
                    }
                ]
            }
        }
    }
</script>