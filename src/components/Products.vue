<template>
  <v-container class="products pb-12 pt-12" fluid>
    <div :class="{ contents: !show }">
      <section-title :title="'Works'" :show="this.show"></section-title>
      <v-container :class="{ contentsShow: show }">
        <v-row justify="center">
          <v-col
            v-for="(item, i) in inprogress"
            :key="i"
            cols="12"
            sm="6"
            md="6"
            lg="6"
            xl="4"
            class="pb-12"
          >
            <v-row class="flex-column">
              <!-- title -->
              <v-col class="system-title text-center">
                <h3>
                  {{ item.title }}
                </h3>
              </v-col>
              <!-- divider -->
              <div class="divider mx-auto my-4"></div>
              <!-- overview -->
              <v-col class="subtitle text-center"><h3>概要</h3></v-col>
              <v-col class="system-desc text-center px-10">
                <h4>{{ item.desc }}</h4>
              </v-col>
              <!-- skills -->
              <v-col class="subtitle text-center mt-6 mb-3"
                ><h3>使用スキル</h3></v-col
              >
              <v-col class="system-desc text-center px-10">
                <v-row class="flex-column"></v-row>
                <v-col
                  v-for="skill in item.skills"
                  :key="skill"
                  class="system-desc text-center py-0"
                >
                  <h4>{{ skill }}</h4>
                </v-col>
              </v-col>
              <!-- link -->
              <v-col class="subtitle text-center mt-6 mb-3"
                ><h3>リンク</h3></v-col
              >
              <v-col class="system-desc text-center px-10">
                <v-row class="flex-column"></v-row>
                <v-col
                  v-for="contents in item.links"
                  :key="contents.link"
                  class="system-desc text-center py-1"
                >
                  <a id="tag" :href="contents.link"
                    ><h4>{{ contents.desc }}</h4></a
                  >
                </v-col>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </v-container>
</template>

<script>
import SectionTitle from "./SectionTitle.vue";
export default {
  props: ["show"],
  data() {
    return {
      inprogress: [
        {
          title:
            "九大 × docomo\n「3密回避実証実験」\nPoC システム, モバイルアプリ開発",
          desc:
            "九州大学とNTTdocomoによる, ポイント付与を用いての3密回避を促す実証実験で使用するサーバやモバイルアプリなどのシステム開発に参加しています。主に九州大学の学生で構成される産学連携プラットフォームである「iQ Lab」として開発に携わっており, システム開発のみでなく, テスターの募集や実験シナリオの考案などの運営やサポート業務も行っています。",
          skills: [
            "Flutter",
            "Firebase Authentification",
            "Firebase Analytics",
            "Firebase Cloud Messaging",
            "Firebase Dynamic Links",
          ],
          links: [
            {
              desc: "プレスリリース",
              link: "https://www.kyushu-u.ac.jp/f/41386/20_11_19.pdf",
            },
            {
              desc: "iQ Lab ページ",
              link:
                "https://iqlab.ninja/iq-lab%e3%80%81%e4%b9%9d%e5%b7%9e%e5%a4%a7%e5%ad%a6xntt%e3%83%89%e3%82%b3%e3%83%a2%e3%81%ae%e5%85%b1%e5%90%8c%e7%a0%94%e7%a9%b6%e3%83%97%e3%83%ad%e3%82%b8%e3%82%a7%e3%82%af%e3%83%88%e3%82%92/",
            },
          ],
        },
        {
          title:
            "バス停混雑度可視化システム\nitocon\nフロント, モバイルアプリ開発",
          desc:
            "九州大学システム情報科学府ヒューマノフィリック研究室のプロジェクトであるバス停の混雑度をリアルタイムで可視化するアプリのシステム開発に参加しています。プロジェクト発足時の対象バス停は4つのみでしたが, 設置センサが増えることやページ更新の効率を考えVue.jsを用いてページビューを再設計しました。また, お気に入りバス停やユーザへの通知機能などの拡張性を持たせるためにiOS/Android対応のモバイルアプリも開発中です。",
          skills: [
            "Vue.js",
            "vuetify(CSS Framework)",
            "Flutter",
            "Firebase Cloud Messaging",
          ],
          links: [
            // { desc: "itocon", link: "https://hub.arakawa-lab.com/itocon" },
            { desc: "研究室ページ", link: "https://arakawa-lab.com/itocon/" },
          ],
        },
        {
          title: "株式会社INNOVATION PLUS\nインターン\nPoC モバイルアプリ開発",
          desc:
            "九州大学の学生とIoTを中心とした事業を展開する企業との, 産学連携とIOT Innovation創出を目的とした組織であるIOT INNOVATION Baseのプロジェクト(IOTII)の一環として, 株式会社INNOVATION PLUSでPoCモバイルアプリ開発インターンを行っています。サービスの予約や支払い, Bluetooth通信機能などが含まれます。",
          skills: ["Flutter"],
          links: [{ desc: "IOT II", link: "https://www.iotii.org/" }],
        },
      ],
      pastworks: [
        {
          title: "ダッシュボード作成",
          desc:
            "保存されているCSVデータから条件を複数選択して情報を表示させるダッシュボードを作成しました。フロントをVue.js, バックエンドをPythonフレームワークであるFlaskを使用しています",
          skill: ["Vue", "Vuetify", "Python", "Flask", "Heroku"],
        },
        // { title: "", desc: "", skill: [] },
      ],
    };
  },
  components: { SectionTitle },
};
</script>

<style scoped>
#tag {
  color: #a7a9be;
}

#tag:hover {
  text-decoration: none;
}

.products {
  background-color: #16161a;
}

.contents {
  opacity: 0;
}

.subtitle {
  color: #ff8906;
}

.system-title {
  color: #fffffe;
}

.divider {
  background-color: #ff8906;
  width: 6rem;
  height: 2px;
}

.subtitle {
  color: #ff8906;
}

.system-desc {
  color: #a7a9be;
}

.contentsShow {
  opacity: 1;
  animation: contentsFadeIn 1s;
}

@keyframes contentsFadeIn {
  0% {
    opacity: 0;
    transform: translateX(15rem);
  }
  100% {
    opacity: 1;
    transform: translateY(0px);
  }
}
</style>
