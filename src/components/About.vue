<template>
  <v-row class="about">
    <v-col>
      <v-row justify="center">
        <v-avatar size="10rem">
          <img src="@/assets/images/my_image.jpg" alt="My Image" />
        </v-avatar>
      </v-row>
      <h1 class="text-center my-name">SHUTA MATSUO</h1>
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
                <h4 class="title-text text-center">
                  {{ item.title }}
                </h4>
              </v-col>
              <div class="divider mx-auto"></div>
              <v-col class="desc text-center">
                <h5>{{ item.desc }}</h5>
              </v-col>
            </v-row>
          </v-col>
        </v-row>
      </v-container>
    </v-col>
  </v-row>
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
.about {
  background-color: #242629;
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
  text-align: center;
}

.desc {
  color: #94a1b2;
}
</style>
