<template  >
  <div class="background-style">
    <v-form ref="form">
      <v-row no-gutters class="">
        <v-col cols="12" sm="6">
          <div v-if="loginOrRegister">
            <v-card height="500" elevation="0" rounded="0" class="pt-5 px-12">
              <v-card-title primary-title> ورود </v-card-title>
              <VCardText>جهت ورود ایمیل و پسورد خود را وارد کنید </VCardText>

              <v-container>
                <v-row>
                  <v-col cols="12">
                    <v-text-field
                      :rules="emailRule"
                      background-color="white"
                      filled
                      color="#ccdcf2"
                      label="ایمیل"
                      outlined
                      placeholder="example@mail.com"
                      append-icon="mdi-email"
                      hint="ایمیل خود را وارد کنید"
                      single-line
                      type="email"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12">
                    <v-text-field
                      :rules="passRule"
                      background-color="white"
                      filled
                      color="#ccdcf2"
                      label="رمز عبور"
                      outlined
                      placeholder="example@mail.com"
                      append-icon="mdi-lock"
                      hint="رمز ورود را وارد کنید"
                      single-line
                      type="password"
                    ></v-text-field>
                  </v-col>
                </v-row>
                <v-btn
                  large
                  class="white--text mt-5"
                  width="100%"
                  color="#5a7bb5"
                  >ورود</v-btn
                >
                <v-container
                  class="d-flex justify-space-between"
                  justify-center
                >
                  <span class="mt-6"
                    >جهت ثبت نام بر روی ایکون مقابل کلیک کنید</span
                  >
                  <v-btn
                    center
                    class="white--text mt-5"
                    width="30%"
                    color="orange"
                    @click="changeLoginToRegister"
                    >ثبت نام
                  </v-btn>
                </v-container>
                <v-container
                  class="d-flex justify-space-between"
                  justify-center
                >
                  <span class="mt-6"
                    >جهت بازیابی رمز عبور بر روی ایکون مقابل کلیک کنید</span
                  >
                  <v-btn
                    center
                    class="white--text mt-5"
                    width="30%"
                    color="red"
                    href="/forgotPassword"
                    >بازیابی رمز
                  </v-btn>
                </v-container>
              </v-container>
            </v-card>
          </div>

          <div v-if="!loginOrRegister">
            <v-card height="500" elevation="0" rounded="0" class="pt-5 px-12">
              <v-card-title primary-title> ثبت نام </v-card-title>
              <VCardText>جهت ثبت نام موارد زیر را تکمیل فرمایید </VCardText>

              <v-container>
                <v-row>
                  <v-col cols="12">
                    <v-text-field
                      background-color="white"
                      filled
                      color="#ccdcf2"
                      label="نام و نام خانوادگی"
                      outlined
                      append-icon="mdi-account"
                      hint="نام و نام خانوادگی خود را وارد کنید "
                      single-line
                      type="email"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12">
                    <v-text-field
                      :rules="emailRule"
                      background-color="white"
                      filled
                      color="#ccdcf2"
                      label="ایمیل"
                      outlined
                      placeholder="example@mail.com"
                      append-icon="mdi-email"
                      hint="ایمیل خود را وارد کنید"
                      single-line
                      type="email"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12">
                    <v-text-field
                      :rules="passRule"
                      background-color="white"
                      filled
                      color="#ccdcf2"
                      label="رمز عبور"
                      outlined
                      placeholder="example@mail.com"
                      append-icon="mdi-lock"
                      hint="رمز ورود را وارد کنید"
                      single-line
                      type="password"
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12">
                    <v-text-field
                      :rules="passRule"
                      background-color="white"
                      filled
                      color="#ccdcf2"
                      label="تکرار رمز ورود "
                      outlined
                      placeholder="example@mail.com"
                      append-icon="mdi-lock"
                      hint="تکرار رمز ورود را وارد کنید"
                      single-line
                      type="password"
                    ></v-text-field>
                  </v-col>
                </v-row>
                <v-btn
                  large
                  class="white--text mt-5"
                  width="100%"
                  color="green "
                  >ثبت نام</v-btn
                >
                <v-container
                  class="d-flex justify-space-between"
                  justify-center
                >
                  <p class="mt-6">اگر عضو هستید بر روی ایکون مقابل بزنید</p>
                  <v-btn
                    center
                    class="white--text mt-5"
                    width="30%"
                    color="red"
                    @click="changeLoginToRegister"
                    >ورود اعضا
                  </v-btn>
                </v-container>
              </v-container>
            </v-card>
          </div>
        </v-col>
        <v-col v-if="WeidthOfScreen" cols="12" sm="6">
          <v-card
            height="700"
            rounded="0 "
            elevation="0"
            img="https://picsum.photos/1920/1080?random"
          >
          </v-card>
        </v-col>
      </v-row>
    </v-form>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      loginOrRegister: true,
      emailRule: [
        (v) => !!v || "ایمیل را وارد کنید",
        (v) => /.+@.+\..+/.test(v) || "ادرس ایمیل صحیح نیست",
      ],

      passRule: [
        (v) => !!v || "رمز را وارد کنید",
        (v) => (v && v.length >= 8) || "حداقل ۸ کاراکتر",
      ],
    };
  },
  methods: {
    changeLoginToRegister() {
      var mmm = this.loginOrRegister;
      this.loginOrRegister = !mmm;
    },
  },
  //  computed:{
  //    calculate(){
  //         this.windowHeight=window.innerWidth
  //    }
  //  }
  computed: {
    WeidthOfScreen() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return false;
        case "sm":
          return true;
        case "md":
          return true;
        case "lg":
          return true;
        case "xl":
          return true;
      }
    },
  },
};
</script>

<style  scoped>
.background-style {
  background-color: white;

  /* background-image: url("/img/backlogin.webp");
    background-repeat: no-repeat;
    background-size: 100% 100%; */
}
.justifyContent {
  padding: 5% 15%;
}
</style>