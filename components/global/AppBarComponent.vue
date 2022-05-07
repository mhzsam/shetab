<template>
  <v-card>
    <v-app-bar
      height="20"
      color="black"
      dark
      shrink-on-scroll
      prominent
      src="https://picsum.photos/1920/1080?random"
      fade-img-on-scroll
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(252,255,0,.7), rgba(2,0,36,.7)"
        ></v-img>
      </template>
      <v-img class="mt-5 mx-5 mb-12" max-width="35" src="logo/logo.png">
      </v-img>
      <v-app-bar-title>شتاب دهنده امین </v-app-bar-title>
      <v-spacer></v-spacer>

      <v-btn color="" class="white--text mt-5" href="/login"
        >ورود
        <v-icon class="">mdi-login-variant</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs color="yellow" background-color="#0A0A0A" show-arrows class="">
          <v-tabs-slider color="yellow"></v-tabs-slider>
          <v-tab v-for="(item, index) in navItem" :key="index" :to="item.link"
            >{{ item.name }}
          </v-tab>
        </v-tabs>
      </template>
    </v-app-bar>
  </v-card>
</template>

<script>
export default {
  name: "AppBarComponent",
  data() {
    return {
      navItem: [
        { name: "خانه ", link: "/" },
        { name: "ناحیه کاربری  ", link: "/dashboard" },
        { name: "دوره ها ", link: "/course" },
        { name: "ثبت استارتاپ ", link: "/startupRegistration" },
        { name: "وبلاگ", link: "/blog" },
      ],
    };
  },
};
</script>

<style  scoped>
</style>