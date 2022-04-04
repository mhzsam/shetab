<template  >
  <div class="background-style">
    <v-form class="" ref="form">
      <v-row no-gutters class="">
        <v-col class="" cols="12">
          <div >
            <v-container>
              <v-layout  align-center justify-center mt-10>
                <v-flex  xs12 sm8 md8>
                  <v-card class="elevation-12 " >
                    <v-toolbar class=" black--text" color="#ccdcf2">
                      <v-toolbar-title>فراموشی رمز ورود </v-toolbar-title>
                    </v-toolbar>

                    <v-stepper class="FP-background" v-model="e6" vertical>
                      <v-stepper-step
                        :complete="e6 > 1"
                        step="1"
                        color="#70def1"
                        class="black--text"
                      >
                        وارد کردن ایمیل
                      </v-stepper-step>

                      <v-stepper-content step="1">
                        <v-form ref="form">
                          <v-text-field
                            v-model="email"
                            :rules="emailRule"
                            required
                            prepend-icon="mdi-email"
                            name="email"
                            label="ایمیل"
                            type="text"

                           
                      background-color="white"
                      filled
                      color="#ccdcf2"
                     
                      outlined
                      placeholder="example@mail.com"
                      append-icon="mdi-email"
                      hint="ایمیل خود را وارد کنید"
                      single-line
                      
                          ></v-text-field>
                        </v-form>
                        <div class="text-left mt-3 mb-5">
                          <v-btn
                            width="20%"
                            color="#5a7bb5"
                            large
                            class="font-weight-bold white--text"
                            @click="submit"
                            >مرحله بعد</v-btn
                          >
                        </div>
                      </v-stepper-content>

                      <v-stepper-step
                        :complete="e6 > 2"
                        step="2"
                        color="#70def1"
                      >
                        رمز بازیابی
                        <small class="mt-1"
                          >در صورت موجود بودن ایمیل رمزی جهت بازیابی رمز ورود
                          ارسال شده است</small
                        >
                      </v-stepper-step>

                      <v-stepper-content step="2">
                        <div class="px-16 mx-16 my-5">
                          <v-otp-input
                            class="otp"
                            length="4"
                            type="number"
                          ></v-otp-input>
                        </div>

                        <div class="text-left mt-3 mb-5">
                          <v-btn
                            width="20%"
                            color="#5a7bb5"
                            large
                            class="font-weight-bold white--text"
                            @click="submit2"
                            >مرحله بعد</v-btn
                          >
                        </div>
                      </v-stepper-content>

                      <v-stepper-step
                        :complete="e6 > 3"
                        step="3"
                        color="#70def1"
                      >
                        رمز جدید را وارد کنید
                      </v-stepper-step>

                      <v-stepper-content step="3">
                        <v-form>
                          <v-text-field
                            :rules="passRule"
                            v-model="password"
                            required
                            prepend-icon="mdi-lock"
                            name="password"
                            label="پسورد"
                            type="password"
                          ></v-text-field>
                          <v-text-field
                            :rules="repassRule"
                            v-model="rePassword"
                            required
                            prepend-icon="mdi-lock"
                            name="rePassword"
                            label="تکرار رمز ورود"
                            type="password"
                          ></v-text-field>
                        </v-form>

                        <div class="text-left mt-3 mb-5">
                          <v-btn
                            width="20%"
                            color="#5a7bb5"
                            large
                            class="white--text font-weight-bold"
                            @click="submit2"
                            >تغییر رمز
                          </v-btn>
                        </div>
                      </v-stepper-content>
                    </v-stepper>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </div>
        </v-col>
      </v-row>
    </v-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
       rePassword: "",
      password: "",
      e6: 1,
      email: "",
      emailRule: [
        (v) => !!v || "ایمیل را وارد کنید",
        (v) => /.+@.+\..+/.test(v) || "ادرس ایمیل صحیح نیست",
      ],

      passRule: [
        (v) => !!v || "رمز را وارد کنید",
        (v) => (v && v.length >= 8) || "حداقل ۸ کاراکتر",
      ],
      repassRule: [
        (v) => !!v || "رمز را وارد کنید",
        (v) => v == this.password || "رمز های عبور یکسان نیستند",
      ],
    };
  },
  methods: {
      submit() {
      if (this.$refs.form.validate()) {
        console.log(this.password);
        this.e6 = 2;
      } else {
        alert("لطفا مقادیر را کامل کنید");
      }
    },
    submit2() {
      if (this.$refs.form.validate()) {
        console.log(this.password);
        this.e6 = 3;
      } else {
        alert("لطفا مقادیر را کامل کنید");
      }
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
.FP-background{
    background-color: #f4f6fc;
}
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