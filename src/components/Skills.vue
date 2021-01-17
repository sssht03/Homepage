<template>
  <v-row class="skills">
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
        class="mx-auto"
        max-width="300"
        min-height="450"
        elevation="3"
        color="#16161a"
        dark
      >
        <v-layout justify-center>
          <v-img :src="item.src" max-height="150" max-width="150"></v-img>
        </v-layout>
        <v-card-title>{{ item.name }}</v-card-title>
        <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>
        <v-divider></v-divider>
        <v-card-text>{{ item.text }}</v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      show: false,
      skillList: [
        {
          name: "Flutter",
          subtitle: "モバイル開発",
          text:
            "iOS, Android対応モバイルアプリケーションの開発経験があります。\nワイヤーフレームワークをもとにしたUI実装, providerを使用したMVVM開発, バックエンドでのサーバとの通信の実装などを行っています。",
          src: require("../assets/images/flutter.png"),
        },
        {
          name: "Vue.js",
          subtitle: "フロントエンド開発",
          text:
            "Vue2を使用したリアクティブな画面の実装経験があります。CSSフレームワークとしてVuetify, プラグインにVue-routerを使用した、ダッシュボードやセンサ情報表示のSPAを開発しています。",
          src: require("../assets/images/vue.png"),
        },
        {
          name: "Python",
          subtitle: "データ分析, Webツール",
          text:
            "データフレームによる簡単なデータのグラフ化やWeb情報のスクレイピング, VueのバックエンドとしてFlaskでデータの受け渡しの実装経験があります。",
          src: require("../assets/images/python.png"),
        },
        {
          name: "Google Apps Script",
          subtitle: "作業効率化",
          text:
            "Spread Sheetの自動更新や, Slackへの定期的なリマインダーや日報の送信機能の実装経験があります。",
          src: require("../assets/images/gas.png"),
        },
        {
          name: "Firebase",
          subtitle: "バックエンドサービス",
          text:
            "Authentificationによる認証, Cloud FiretoreやRealtime Databaseによるデータベース作成, Cloud MessagingによるモバイルアプリへのPush通知送信, Dynamic LinksによるモバイルとWebの動的なルーティング, Analyticsによる分析データ収集の実装経験があります。",
          src: require("../assets/images/firebase.png"),
        },
        {
          name: "Fitbit",
          subtitle: "fitbit SDK",
          text:
            "スマートウォッチであるfitbitのアプリケーション開発で、画面で選択した情報のWebへの送信や、位置情報を利用した機能の実装経験があります。",
          src: require("../assets/images/fitbit.png"),
        },
      ],
    };
  },
};
</script>

<style>
.skills {
  background-color: #242629;
}
</style>