<template>
  <v-row justify="center">
    <v-timeline align-top dense>
      <v-timeline-item
        color="#7f5af0"
        small
        v-for="(item, i) in years"
        :key="i"
      >
        <v-row class="">
          <v-col cols="3" sm="3" md="3" lg="3" xl="4">
            <h3 class="text-start">
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
</template>

<script>
export default {
  data() {
    return {
      years: [
        {
          year: "2016/3",
          desc: "長崎県立 長崎東高等学校 卒業",
        },
        {
          year: "2016/4",
          desc: "九州大学工学部 電気情報工学科 入学",
        },
        {
          year: "2020/3",
          desc: "九州大学工学部 電気情報工学科 卒業",
        },
        {
          year: "2020/4",
          desc: "九州大学大学院 システム情報科学府 研究生 入学",
        },
        {
          year: "2021/3",
          desc: "九州大学大学院 システム情報科学府 研究生 卒業",
        },
        {
          year: "2021/4",
          desc: "九州大学大学院 システム情報科学府 入学予定",
        },
      ],
    };
  },
};
</script>

<style>
.career-desc {
  color: #94a1b2;
}
</style>
