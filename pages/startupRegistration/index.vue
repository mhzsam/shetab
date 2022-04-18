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
            <v-row dense no-gutters class="mt-2">
              <v-col offset="0" cols="12" md="6" class="ma-0 pa-0">
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
              <v-col offset="0" cols="12" md="6">
                <div class="d-flex justify-center">
                  <v-img
                    class="rounded-lgs"
                    max-width="450"
                    src="/img/wallpaper/start.jpg"
                  >
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
                  v-model="obj.name"
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="نام "
                  outlined
                  hint="نام را وارد کنید "
                ></v-text-field>
                <v-text-field
                  v-model="obj.family"
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label=" نام خانوادگی "
                  outlined
                  hint="نام خانوادگی را وارد کنید "
                ></v-text-field>
                <v-text-field
                  v-model="obj.post"
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label=" مسئولیت "
                  outlined
                  hint=" مسئولیت را وارد کنید "
                ></v-text-field>

                ّ
              </v-col>
              <v-col cols="12" md="6">
                <v-select
                  v-model="obj.educationLevel"
                  :items="items"
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label="تحصیلات  "
                  outlined
                ></v-select>
                <v-text-field
                  v-model="obj.education"
                  background-color="white"
                  filled
                  color="#ccdcf2"
                  label=" رشته "
                  outlined
                  hint=" رشته را وارد کنید "
                ></v-text-field>
                <v-row>
                  <v-col cols="8">
                    <v-slider
                      v-model="obj.age"
                      class="mt-8"
                      color="teal darken-3"
                      label="سن"
                      hint="تفریبی"
                      min="18"
                      max="50"
                      thumb-label="always"
                      ticks="always"
                    ></v-slider
                  ></v-col>
                  <v-col cols="4"
                    ><v-btn
                      min-height="50"
                      dark
                      color="teal darken-3"
                      block
                      @click="AddToTable"
                      >ثبت
                    </v-btn></v-col
                  >
                </v-row>
              </v-col>
            </v-row>

            <v-row class="mt-n10 mb-5">
              <v-col cols="12">
                <v-card>
                  <v-card-title>تیم ثبت شده</v-card-title>

                  <v-simple-table>
                    <thead>
                      <tr>
                        <th>نام</th>
                        <th>نام خانوادگی</th>
                        <th>مسئولیت</th>
                        <th>تحصیلات</th>
                        <th>رشته</th>
                        <th>سن</th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr v-for="item in tabaleObj" :key="item.name">
                        <td>{{ item.name }}</td>
                        <td>{{ item.family }}</td>
                        <td>{{ item.post }}</td>
                        <td>{{ item.educationLevel }}</td>
                        <td>{{ item.education }}</td>
                        <td>{{ item.age }}</td>
                      </tr>
                    </tbody>
                  </v-simple-table>
                </v-card>
              </v-col>
            </v-row>

            <v-btn dark color="green" @click="e1 = 3"> ادامه </v-btn>

            <v-btn color="red" text> لغو </v-btn>
          </v-card>
        </v-stepper-content>
      </v-stepper-items>

      <v-stepper-items>
        <v-stepper-content step="3">
          <v-card flat class="">
            <v-textarea
              background-color="white"
              outlined
              filled
              clearable
              clear-icon="mdi-close-circle"
              label="متن"
              placeholder="متن خود را تایپ کنید "
            ></v-textarea>

            <v-btn dark color="green" @click="e1 = 1"> ادامه </v-btn>

            <v-btn color="red" text> لغو </v-btn>
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
      obj: {
        name: "",
        family: "",
        post: "",
        educationLevel: "",
        education: "",
        age: "",
      },
      tabaleObj: [
       
      ],
      items: ["دیپلم", "لیسانس", "فوق لیسانس", "دکترا"],
      e1: 1,
    };
  },
  methods: {
    AddToTable() {
      const newObj={
        name:this.obj.name,
        family:this.obj.family,
        post:this.obj.post,
        educationLevel:this.obj.educationLevel,
        education:this.obj.educationLevel,
        age:this.obj.age,
      }
     this.tabaleObj.push(newObj)
     
    },
  },
};
</script>

<style scoped>
.title-page {
  background-color: #f4f6fc;
  font-weight: bold;
}
</style>
