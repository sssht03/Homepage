<template>
  <v-footer dark padless>
    <v-card class="flex" flat tile color="#2e2f3e">
      <v-card-text class="text-center">
        <v-btn
          v-for="(icon, i) in icons"
          :key="i"
          class="mx-6"
          :href="icon.link"
          icon
        >
          <v-icon size="32px">
            {{ icon.name }}
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
    icons: [
      { name: "mdi-github", link: "https://github.com/sssht03" },
      {
        name: "mdi-instagram",
        link: "https://www.instagram.com/sssht03/?hl=ja",
      },
    ],
  }),
};
</script>