<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card class="logo py-4 d-flex justify-center">
        <YamiIcon />
      </v-card>
      <v-card>
        <v-card-title class="headline">
          MiyanoYami's website
        </v-card-title>
        <v-card-text>
          <p>なんかかく</p>
          <hr class="my-3">
          <a
            href="https://github.com/miyanoyami/yamihouse"
            target="_blank"
            rel="noopener noreferrer"
          >
            MiyanoYami GitHub
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            to="/inspire"
          >
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>
