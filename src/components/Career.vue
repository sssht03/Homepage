<template>
  <v-container class="career pb-12" fluid>
    <v-row>
      <v-col>
        <section-title :title="'Career'"></section-title>
        <v-row justify="center">
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

<style>
.career {
  background-color: #16161a;
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
</style>
