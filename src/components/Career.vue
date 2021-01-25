<template>
  <v-container class="career pb-12" fluid>
    <v-row :class="{ contents: !show }">
      <v-col>
        <section-title :title="'Career'" :show="show"></section-title>
        <v-row justify="center" :class="{ contentsShow: show }">
          <v-timeline
            align-top
            dark
            class="timeline mx-10"
            :dense="$vuetify.breakpoint.smAndDown"
          >
            <v-timeline-item
              color="#ff8906"
              small
              v-for="(item, i) in years"
              :key="i"
            >
              <v-row>
                <v-col>
                  <h3 class="text-start career-year">
                    {{ item.year }}
                  </h3>
                </v-col>
                <v-col cols="12" sm="12" md="12" lg="12" xl="12">
                  <h4 class="text-start career-desc">
                    {{ item.desc }}
                  </h4>
                </v-col>
              </v-row>
            </v-timeline-item>
          </v-timeline>
        </v-row>
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
      years: [
        {
          year: "2016/3",
          desc: "長崎県立\n長崎東高等学校\n卒業",
        },
        {
          year: "2016/4",
          desc: "九州大学工学部\n電気情報工学科\n入学",
        },
        {
          year: "2020/3",
          desc: "九州大学工学部\n電気情報工学科\n卒業",
        },
        {
          year: "2020/4",
          desc: "九州大学大学院\nシステム情報科学府(研究生)\n入学",
        },
        {
          year: "2021/3",
          desc: "九州大学大学院\nシステム情報科学府(研究生)\n卒業予定",
        },
        {
          year: "2021/4",
          desc: "九州大学大学院\nシステム情報科学府\n入学予定",
        },
      ],
    };
  },
};
</script>

<style scoped>
.career {
  background-color: #16161a;
}

.contents {
  opacity: 0;
}

.career-year {
  color: #ff8906;
}

.career-desc {
  color: #94a1b2;
}

.timeline {
  z-index: 0;
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
