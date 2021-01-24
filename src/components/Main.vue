<template>
  <div>
    <header>
      <v-app-bar fixed color="rgba(114, 117, 126, 0.9)" height="60">
        <v-container fluid>
          <v-row align-content="center" justify="center">
            <v-btn
              text
              :x-large="$vuetify.breakpoint.mdAndUp"
              :small="$vuetify.breakpoint.smAndDown"
              v-for="(item, i) in contentsList"
              :key="i"
              ><a
                href="#"
                id="btn-anker"
                v-scroll-to="`#${item.title}`"
                @click="sectionSelect(i)"
              >
                <div v-bind:class="{ selected: item.show }">
                  {{ item.title }}
                </div>
              </a>
            </v-btn>
          </v-row>
        </v-container>
      </v-app-bar>
    </header>
    <about id="about"></about>
    <career id="career"></career>
    <skills id="skills"></skills>
    <products id="works"></products>
    <Footer></Footer>
  </div>
</template>

<script>
import Vue from "vue";
import VueScrollTo from "vue-scrollto";
Vue.use(VueScrollTo);

import About from "./About.vue";
import Career from "./Career.vue";
import Footer from "./Footer.vue";
import Products from "./Products.vue";
import Skills from "./Skills.vue";

export default {
  name: "Main",
  components: { About, Career, Skills, Products, Footer },
  data() {
    return {
      scrollY: 0,
      sectionOffsetTop: [],
      contentsList: [
        { title: "about", show: true },
        { title: "career", show: false },
        { title: "skills", show: false },
        { title: "works", show: false },
      ],
    };
  },
  mounted() {
    window.addEventListener("scroll", () => {
      this.pushScrollY();
      this.currentNavi();
    });
    window.addEventListener("resize", () => {
      this.pushScrollY();
      this.currentNavi();
    });
    this.pushElementOffsetTop();
  },
  methods: {
    sectionSelect: function (index) {
      for (var i = 0; i < this.contentsList.length; i++) {
        if (i == index) {
          this.contentsList[i].show = true;
        } else this.contentsList[i].show = false;
      }
    },
    currentNavi() {
      if (
        this.scrollY >= this.sectionOffsetTop[0] &&
        this.scrollY < this.sectionOffsetTop[1]
      ) {
        this.sectionSelect(0);
      } else if (
        this.scrollY >= this.sectionOffsetTop[1] &&
        this.scrollY < this.sectionOffsetTop[2]
      ) {
        this.sectionSelect(1);
      } else if (
        this.scrollY >= this.sectionOffsetTop[2] &&
        this.scrollY < this.sectionOffsetTop[3]
      ) {
        this.sectionSelect(2);
      } else if (this.scrollY >= this.sectionOffsetTop[3]) {
        this.sectionSelect(3);
      }
    },
    pushScrollY() {
      this.scrollY = window.scrollY;
    },
    pushElementOffsetTop() {
      const targets = ["about", "career", "skills", "works"];
      targets.forEach((target) => {
        const element = document.getElementById(target);
        const offsetTop = Math.round(
          window.scrollY + element.getBoundingClientRect().top - 60
        );
        this.sectionOffsetTop.push(offsetTop);
      });
    },
  },
};
</script>

<style>
#btn-anker {
  text-decoration: none;
  color: #fffffe;
}
.selected {
  color: #f25f4c;
}
</style>

