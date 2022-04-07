<template>
  <v-card >
    <v-app-bar
      height="20"
      color="#5B7BB6"
      dark
      shrink-on-scroll
      prominent
      src="https://picsum.photos/1920/1080?random"
      fade-img-on-scroll
      
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(100,115,201,.7), rgba(25,32,72,.7)"
        ></v-img>
      </template>

      <v-app-bar-title>شتاب دهنده امین </v-app-bar-title>
      <v-spacer></v-spacer>
      <v-img class="mt-5 mx-5 mb-12" max-width="150" src="img/logow.png">
      </v-img>
      <v-btn color="" class="white--text mt-5" href="/login"
        >ورود
        <v-icon class="">mdi-login-variant</v-icon>
      </v-btn>

      <template v-slot:extension>
        <v-tabs background-color="#5B7BB6" show-arrows class="">
          <v-tab v-for="(item, index) in navItem" :key="index"  :to="item.link"
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
        { name: "دوره ها ", link: "/2" },
        { name: "تیم من ", link: "/3" },
        { name: "وبینار ", link: "/4" },
        { name: "ثبت استارتاپ ", link: "/5" },
        { name: "ادمین", link: "/6" },
        { name: "تعرفه ", link: "/7" },
          
      ],
      
    };
  },
};
</script>

<style  scoped>
</style>