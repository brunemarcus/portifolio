<template>
    
    <div id="habilidades">
        <v-row no-gutters>
            <v-col
                class="mb-3 mr-5"
                v-for="item in skill" :key="item.title"
                cols="12"
                sm="4"
            >
                {{ item.title }}
                <v-progress-linear
                    v-bind:color="item.color"
                    buffer-value="0"
                    v-bind:value="item.value"
                    stream
            ></v-progress-linear>
            </v-col>
        </v-row>
    </div>

</template>

<script>
    export default {
        data() {
            return {
                skill:
                [
                    {
                        title: 'PHP',
                        color: 'light-blue',
                        value: '85'
                    },
                    {
                        title: 'Laravel',
                        color: 'orange',
                        value: '45'
                    },
                    {
                        title: 'Javascript',
                        color: 'red',
                        value: '45'
                    },
                    {
                        title: 'VueJS',
                        color: 'green',
                        value: '35'
                    },
                    {
                        title: 'HTML5',
                        color: 'lime',
                        value: '90'
                    },
                    {
                        title: 'CSS3',
                        color: 'pink darken-4s',
                        value: '80'
                    },
                    {
                        title: 'MySQL',
                        color: 'purple darken-3',
                        value: '65'
                    },
                    {
                        title: 'MySQL Server',
                        color: 'purple lighten-1',
                        value: '65'
                    },
                    {
                        title: 'Nginx',
                        color: 'indigo lighten-1',
                        value: '35'
                    },
                    {
                        title: 'Apache',
                        color: 'teal lighten-1',
                        value: '55'
                    },
                    {
                        title: 'Git',
                        color: 'cyan darken-4',
                        value: '55'
                    },
                    {
                        title: 'Linux',
                        color: 'light-green darken-1',
                        value: '55'
                    }
                ]
            }
        }
    }
</script>