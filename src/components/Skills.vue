<template>
  <v-container class="skills pb-12" fluid>
    <v-row class="flex-column" :class="{ contents: !show }">
      <v-col>
        <section-title :title="'Skills'" :show="this.show"></section-title>
      </v-col>
      <v-row justify="center" class="ma-0" :class="{ contentsShow: show }">
        <v-col
          v-for="(item, i) in skillList"
          :key="i"
          cols="12"
          sm="6"
          md="4"
          lg="4"
          xl="4"
        >
          <v-card
            class="mx-auto py-6 skill-card"
            max-width="280"
            elevation="3"
            @click="item.show = !item.show"
            dark
          >
            <v-layout justify-center>
              <v-img
                :src="item.src"
                :alt="item.name"
                max-height="150"
                max-width="150"
              ></v-img>
            </v-layout>
            <v-card-title>{{ item.name }}</v-card-title>
            <v-row justify="space-between" class="mx-auto">
              <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>
              <v-card-actions>
                <v-btn icon>
                  <v-icon>{{
                    item.show ? "mdi-chevron-up" : "mdi-chevron-down"
                  }}</v-icon>
                </v-btn>
              </v-card-actions>
            </v-row>
            <v-expand-transition>
              <div v-show="item.show">
                <v-divider></v-divider>
                <v-card-text>{{ item.text }}</v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </v-row>
  </v-container>
</template>

<script>
import SectionTitle from "./SectionTitle.vue";
export default {
  props: ["show"],
  components: { SectionTitle },
  data() {
    return {
      skillList: [
        {
          name: "Flutter",
          subtitle: "モバイル開発",
          text:
            "iOS, Android対応モバイルアプリケーションの開発経験があります。\nワイヤーフレームワークをもとにしたUI実装, providerを使用したMVVM開発, バックエンドでのサーバとの通信の実装などを行っています。",
          src: require("../assets/images/flutter.png"),
          show: false,
        },
        {
          name: "Vue.js",
          subtitle: "フロントエンド開発",
          text:
            "Vue2を使用したリアクティブ画面, レスポンシブ画面の実装経験があります。CSSフレームワークとしてVuetify, プラグインにVue-routerを使用した、ダッシュボードやセンサ情報表示のSPAを開発しています。",
          src: require("../assets/images/vue.png"),
          show: false,
        },
        {
          name: "Python",
          subtitle: "データ分析, Webツール",
          text:
            "データフレームによる簡単なデータのグラフ化やWeb情報のスクレイピング, VueのバックエンドとしてFlaskでデータの受け渡しの実装経験があります。",
          src: require("../assets/images/python.png"),
          show: false,
        },
        {
          name: "Google Apps Script",
          subtitle: "作業効率化",
          text:
            "Spread Sheetの自動更新や, Slackへの定期的なリマインダーや日報の送信機能の実装経験があります。",
          src: require("../assets/images/gas.png"),
          show: false,
        },
        {
          name: "Firebase",
          subtitle: "バックエンドサービス",
          text:
            "Authentificationによる認証, Cloud FiretoreやRealtime Databaseによるデータベース作成, Cloud MessagingによるモバイルアプリへのPush通知送信, Dynamic LinksによるモバイルとWebの動的なルーティング, Analyticsによる分析データ収集の実装経験があります。",
          src: require("../assets/images/firebase.png"),
          show: false,
        },
        {
          name: "Fitbit",
          subtitle: "fitbit SDK",
          text:
            "スマートウォッチであるfitbitのアプリケーション開発で、画面で選択した情報のWebへの送信や、位置情報を利用した機能の実装経験があります。",
          src: require("../assets/images/fitbit.png"),
          show: false,
        },
      ],
    };
  },
};
</script>

<style scoped>
.skills {
  background-color: #242629;
}

.contents {
  opacity: 0;
}

.contentsShow {
  opacity: 1;
  animation: contentsFadeIn 1s;
}

@keyframes contentsFadeIn {
  0% {
    opacity: 0;
    transform: translateY(15rem);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
</style>
