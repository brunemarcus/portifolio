<template>
    <!-- Portifolio -->
    <div id="portifolio">
        
        <v-row no-gutters>
            <v-col 
                v-for="item in portifolio" 
                :key="item.title"
                cols="12"
                sm="4"
            > 
            <v-card class="mb-3" max-width="400" height="350px">
                <v-img
                    class="white--text align-end"
                    height="200px"
                    :src="require(`@/assets/images/${item.image}`)" 
                >
                    <v-card-title v-text="item.title"></v-card-title>
                </v-img>
                <v-card-subtitle class="pb-0" v-text="item.subtitle"></v-card-subtitle>
                <v-card-text class="text--primary">
                    <div v-text="item.overview"></div>
                </v-card-text>
                <v-card-actions>
                    <v-btn 
                        color="blue" 
                        :href="`${item.linkButton}`"
                        target="_blank"
                        text 
                        v-text="item.nameButton">
                    </v-btn>
                </v-card-actions>
            </v-card>
            </v-col>
        </v-row>

    </div>
</template>

<script>
    export default {
        data() {
            return {
                portifolio: 
                [
                    {
                        title: "Escala",
                        subtitle: "Hackathon CCR 2 Edição",
                        image: "escala.png",
                        overview: "O projeto tem o objetivo de diminuir o índice de evasão escolar.",
                        nameButton: "Visitar",
                        linkButton: "https://github.com/Gabriel52/SchoolChallenge"
                    },
                    {
                        title: "Movies Shade",
                        subtitle: "Most Popular Movies",
                        image: "movies.png",
                        overview: "Movies Shade é uma aplicação web básica que mostra os filmes mais populares do momento.",
                        nameButton: "Visitar",
                        linkButton: "https://github.com/brunemarcus/MovieShade"
                    },
                    {
                        title: "Karatê Class",
                        subtitle: "Agendamento de Aulas",
                        image: "karate.png",
                        overview: "Aplicação desevolvida com PHP 7 e Laravel 8 para agendar aulas de Karatê.",
                        nameButton: "Visitar",
                        linkButton: "https://github.com/brunemarcus/MySystemLabs"
                    }
                ]
            }
        }
    }
</script>