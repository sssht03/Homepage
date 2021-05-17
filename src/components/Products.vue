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
              <!-- term -->
              <v-col class="subtitle text-center mt-6 mb-3"
                ><h3>期間</h3></v-col
              >
              <v-col class="system-desc text-center px-10 py-0">
                <h4>{{ item.term }}</h4>
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
          term: "2020/9 ~",
          desc:
            "九州大学とNTTdocomoによる, ポイント付与を用いての3密回避を促す実証実験で使用するサーバやモバイルアプリなどのシステム開発に参加しています。主に九州大学の学生で構成される産学連携プラットフォームである「iQ Lab」と言う組織のエンジニアチームとしてシステムの開発や業務効率改善ツールの作成などに携わっています。 iQ Lab はシステム開発や実験シナリオの考案と運営, テスターの募集などを行っています。 エンジニアチームは実験で用いられるクロスプラットフォームでのモバイルアプリやデータベース, API サーバの設計から開発, 運用まで一貫して行っています。 特に私はモバイルアプリ開発をメインで担当しており, フレームワークとして Flutter を用いています。デザイナーチームと UI 設計について議論しながら画面の開発, API サーバとの連携を行っています。また、私はプロジェクト全体のマネジメント業務も行っており、エンジニア班以外の企画、広報班の進捗管理やミーティングの設定と進行、さらに企業や大学の研究者の方々への報告や実験を進めるにあたっての相談、議論にも参加しています。",
          skills: ["Flutter", "Firebase"],
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
          term: "2020/06 ~",
          desc:
            "九州大学システム情報科学府ヒューマノフィリック研究室のプロジェクトであるバス停の現在や予測される混雑度、食堂の混雑度をリアルタイムで可視化するwebアプリのシステム開発にチームリーダーとして参加しています。プロジェクト発足時の対象バス停は4つのみでしたが, 設置センサが増えることやページ更新の効率を考えVue.jsを用いてページビューを再設計しました。大学の総長や理事から大学全体へ周知したいとの要望をいただくことがあり、バス停11箇所と食堂5箇所へのアップデートを授業が始まっている中、約1ヶ月で行いました。この情報はサイネージとしてキャンパス全体に設置案が出ており, 混雑度情報を見た学生の行動変容が起こるかの研究が開始される予定です。また, お気に入りのバス停/食堂の登録やユーザへの通知機能などの拡張性を持たせるためにiOS/Android対応のモバイルアプリも開発中予定です。",
          skills: ["Vue.js", "Vuetify", "Flutter"],
          links: [
            { desc: "itocon", link: "https://hub.arakawa-lab.com/itocon" },
            { desc: "研究室ページ", link: "https://arakawa-lab.com/itocon/" },
          ],
        },
        {
          title: "株式会社INNOVATION PLUS\nインターン\nPoC モバイルアプリ開発",
          term: "2020/12 ~ 2021/4",
          desc:
            "九州大学の学生とIoTを中心とした事業を展開する企業との, 産学連携とIOT Innovation創出を目的とした組織であるIOT INNOVATION Baseのプロジェクト（IOTII）の一環として, 株式会社INNOVATION PLUSでPoCモバイルアプリ開発インターン経験があります。Flutter によるクロスプラットフォームで開発を行い, UI プロトタイプや画面設計書からモデルやUI画面に落とし込んだ結果を踏まえての改善点の議論や, アプリ内で使用する Bluetooth 機能の調査, テスト実装などに携わっていました。 INNOVATION PLUS のオフィスは東京にあり, 私が在住する福岡から離れているため全ての業務, ミーティングをオンラインで行いました。",
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
