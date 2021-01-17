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
            <h4 class="title-text">{{ item.title }}</h4>
          </v-col>

          <v-col class="desc"
            ><h4>{{ item.desc }}</h4></v-col
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
