<template>
  <v-container>
    <v-row justify="center">
      <v-avatar size="15rem">
        <img src="@/assets/images/my_image.jpg" alt="My Image" />
      </v-avatar>
    </v-row>
    <h1 class="text-center mt-10 my-name">SHUTA MATSUO</h1>
    <v-row class="pa-6">
      <v-col
        class="py-10"
        v-for="item in myProfile"
        :key="item[1]"
        cols="6"
        sm="6"
        md="4"
        lg="4"
        xl="4"
      >
        <v-row class="flex-column" justify="center" align-content="center">
          <v-col class="title">
            <h4 class="title-text">{{ item[0] }}</h4>
          </v-col>

          <v-col class="desc"
            ><h4>{{ item[1] }}</h4></v-col
          >
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      myProfile: [
        ["職業", "学生"],
        ["所属", "九州大学工学府\nシステム情報工学科"],
        ["誕生日", "1998/03/11"],
        ["出身地", "長崎"],
        ["在住", "福岡"],
        ["好きなこと", "お酒を飲む\nバンドを聴く"],
      ],
    };
  },
};
</script>

<style>
.my-name {
  color: #fffffe;
}
.title {
  border-bottom: 2px solid #7f5af0;
}

.title-text {
  text-align: center;
  color: #fffffe;
}

.desc {
  text-align: center;
  color: #94a1b2;
}
</style>
