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
      <v-container v-show="false" class="px-12">
        <h1 class="text-center pa-8" style="font-size: 3rem; color: red">
          Special Thank for Liming
        </h1>
        <h1 class="text-center py-8" style="font-size: 2rem">
          極秘特別連載「周と周汰の情熱」
        </h1>
        <v-row justify="center" flex-column>
          <v-col class="text-center" v-for="(item, i) in text" :key="i">
            <v-col>
              <h2>第{{ i + 1 }}話「{{ item.title }}」</h2>
            </v-col>

            <v-col class="text-left">
              <h4>{{ item.contents }}</h4>
            </v-col>
          </v-col>
        </v-row>
      </v-container>
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
    text: [
      {
        title: "出会い",
        contents:
          "あの日、彼らは出会ってしまった。\nそれは初夏を感じる程度の熱だっただろうか、いやそれ以上の何かが、松尾の内側から込み上がる。\n火山のように力強く、流れ星のように繊細で、日の出のように温かい。\n\nこの気持ちは一体なんなのだろう。\tそれは一瞬の動揺だったが、周は完全に理解した。\nこの日、僕らは出会ってしまったんだ、と。\nもう後には引けないのだ、と。",
      },
    ],
  }),
};
</script>
