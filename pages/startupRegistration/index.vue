<template>
  <div>
    <div>
      <v-card-title class="text-center title-page py-3">
        <v-icon class="mx-2" color="black">mdi-arrow-left-bold-circle</v-icon>

        <span class="">ثبت استارتاپ </span>
      </v-card-title>
    </div>
    <v-stepper v-model="e1">
      <v-stepper-header>
        <v-stepper-step color="#5a7bb5 " :complete="e1 > 1" step="1">
          مشخصات استارتاپ
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step color="#5a7bb5 " :complete="e1 > 2" step="2">
          مشخصات تیم
        </v-stepper-step>

        <v-divider></v-divider>

        <v-stepper-step color="#5a7bb5" step="3"> توضیحات </v-stepper-step>
      </v-stepper-header>

      <v-stepper-items>
        <v-stepper-content step="1">
          <v-card flat class="">
            <v-row class="mt-2">
              <v-col cols="12" md="6">
                <v-text-field
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="نام  کسب و کار"
                  outlined
                  hint="نام  کسب و کار را وارد کنید "
                ></v-text-field>
                <v-text-field
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="موضوع"
                  outlined
                  hint="موضوع ارد کنید "
                ></v-text-field>
                <v-text-field
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="شاخه فعالیت"
                  outlined
                  hint="شاخه فعالیت ارد کنید "
                ></v-text-field>
                <v-btn dark color="green" @click="e1 = 2"> ادامه </v-btn>

                <v-btn color="red" text> لغو </v-btn>ّ
              </v-col>
              <v-col cols="12" md="6">
                <div class="d-flex justify-center">
                  <v-img class="rounded-lgs"  max-width="450" src="/img/wallpaper/start.jpg">
                  </v-img>
                </div>
              </v-col>
            </v-row>
          </v-card>
        </v-stepper-content>
      </v-stepper-items>

      
      <v-stepper-items>
        <v-stepper-content step="2">
          <v-card flat class="">
            <v-row class="mt-2">
              <v-col cols="12" md="6">
                <v-text-field
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="نام  کسب و کار"
                  outlined
                  hint="نام  کسب و کار را وارد کنید "
                ></v-text-field>
                <v-text-field
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="موضوع"
                  outlined
                  hint="موضوع ارد کنید "
                ></v-text-field>
                <v-text-field
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="شاخه فعالیت"
                  outlined
                  hint="شاخه فعالیت ارد کنید "
                ></v-text-field>
                <v-btn dark color="green" @click="e1 = 2"> ادامه </v-btn>

                <v-btn color="red" text> لغو </v-btn>ّ
              </v-col>
              <v-col cols="12" md="6">
                
              </v-col>
            </v-row>
          </v-card>
        </v-stepper-content>
      </v-stepper-items>
    </v-stepper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      e1: 1,
    };
  },
};
</script>

<style scoped >
.title-page {
  background-color: #f4f6fc;
  font-weight: bold;
}
</style>