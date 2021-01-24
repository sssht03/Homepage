<template>
  <v-footer dark padless>
    <v-card class="flex" flat tile color="#2e2f3e">
      <v-card-text class="text-center">
        <v-btn v-for="icon in icons" :key="icon" class="mx-6" icon>
          <v-icon size="32px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="py-4 text-center">
        ©︎ {{ new Date().getFullYear() }} — <strong>Shuta Matsuo</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: ["mdi-twitter", "mdi-github", "mdi-instagram"],
  }),
};
</script>