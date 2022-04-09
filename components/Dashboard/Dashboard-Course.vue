<template>
  <div>
    <v-row no-gutters>
      <v-col cols="12" md="12">
        <v-card class="ma-5">
          <div>
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-briefcase</v-icon>
              دوره های خرید شده
            </v-card-title>
            <v-divider inset></v-divider>
            <v-row class="py-5 ma-5">
              <v-col cols="6" sm="2" class="on-hover">
                <a style="text-decoration: none" href="">
                  <v-img src="/img/course/1.png"></v-img>
                  <v-btn color="#f4f6fc" class="py-5 active" block
                    >دوره شماره 1
                  </v-btn>
                </a>
              </v-col>
              <v-col cols="6" sm="2" class="on-hover">
                <a style="text-decoration: none" href="">
                  <v-img src="/img/course/2.png"></v-img>
                  <v-btn color="#f4f6fc" class="py-5 active" block
                    >دوره شماره 2
                  </v-btn>
                </a>
              </v-col>
              <v-col cols="6" sm="2" class="on-hover">
                <a style="text-decoration: none" href="">
                  <v-img src="/img/course/3.png"></v-img>
                  <v-btn color="#f4f6fc" class="py-5 active" block
                    >دوره شماره 3
                  </v-btn>
                </a>
              </v-col>
              <v-col cols="6" sm="2" class="on-hover">
                <a style="text-decoration: none" href="">
                  <v-img src="/img/course/4.png"></v-img>
                  <v-btn color="#f4f6fc" class="py-5 active" block
                    >دوره شماره 4
                  </v-btn>
                </a>
              </v-col>
              <v-col cols="6" sm="2" class="on-hover">
                <a style="text-decoration: none" href="">
                  <v-img src="/img/course/5.png"></v-img>
                  <v-btn color="#f4f6fc" class="py-5 active" block
                    >دوره شماره 5
                  </v-btn>
                </a>
              </v-col>
             
            </v-row>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Dashboard-Course",
  data() {
    return {};
  },
};
</script>

<style scoped>
.on-hover:hover {
  margin-top: -4px !important;

  border-radius: 5px;
}
.on-hover {
  transition: margin 0.3s;
}
.active:hover {
  background-color: #4c83f0 !important;
  color: aliceblue;
}
</style>
