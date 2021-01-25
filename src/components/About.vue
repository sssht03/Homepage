<template>
  <v-container class="about py-12" fluid>
    <v-row :class="{ contents: !show }">
      <v-col>
        <section-title :title="'About'" :show="this.show"></section-title>
        <div :class="{ contentsShow: show }">
          <v-row justify="center" class="py-4">
            <v-avatar size="10rem">
              <img src="@/assets/images/my_image.jpg" alt="My Image" />
            </v-avatar>
          </v-row>
          <div>
            <h1 class="text-center my-name py-10">SHUTA MATSUO</h1>
            <v-container>
              <v-row justify="center">
                <v-col
                  v-for="item in myProfile"
                  :key="item[1]"
                  cols="6"
                  sm="4"
                  md="4"
                  lg="4"
                  xl="4"
                >
                  <v-row class="flex-column">
                    <v-col>
                      <h3 class="title-text text-center">
                        {{ item.title }}
                      </h3>
                    </v-col>
                    <div class="divider mx-auto"></div>
                    <v-col class="desc text-center">
                      <h4>{{ item.desc }}</h4>
                    </v-col>
                  </v-row>
                </v-col>
              </v-row>
            </v-container>
          </div>
        </div>
      </v-col>
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
      myProfile: [
        { title: "職業", desc: "学生" },
        { title: "所属", desc: "九州大学大学院\nシステム情報科学府" },
        { title: "誕生日", desc: "1998/03/11" },
        { title: "出身地", desc: "長崎" },
        { title: "在住", desc: "福岡" },
        { title: "好きなこと", desc: "お酒を飲む\nバンドを聴く" },
      ],
    };
  },
};
</script>

<style scoped>
.about {
  background-color: #242629;
  padding-top: 50px;
}

.contents {
  opacity: 0;
}

.my-name {
  color: #fffffe;
}

.title-text {
  color: #fffffe;
}

.divider {
  background-color: #ff8906;
  width: 6rem;
  height: 2px;
}

.desc {
  color: #94a1b2;
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
    transform: translateX(0);
  }
}
</style>
