<template>
    <v-toolbar>
    <v-tabs
      dark
      background-color="primary"
      grow
    >
      <v-tab>
        <v-badge
          color="pink"
          dot
        >
          Valores
        </v-badge>
      </v-tab>

      <v-tab
        href="#habilidades"
      >
        <v-badge
          color="green"
        >
          Habilidades
        </v-badge>
      </v-tab>

      <v-tab>
        <v-badge
          color="deep-purple accent-4"
          icon="mdi-vuetify"
        >
          Portifólio
        </v-badge>
      </v-tab>
    </v-tabs>
  </v-toolbar>
</template>