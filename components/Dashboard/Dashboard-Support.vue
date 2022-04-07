<template>
  <div>
    <v-row no-gutters>
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="370px">
          <div>
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-account-supervisor-outline</v-icon>
              اخرین تیکن ها
            </v-card-title>
            <v-divider inset></v-divider>
            <v-flex mt-5 d-flex justify-center>
              <v-btn
                width="70%"
                class=""
                height="50"
                elevation="3"
                color="#f4f6fc"
                right
                @click="dialogOn"
                >تیکت 1 تاریخ 12/12/01</v-btn
              >
            </v-flex>
            <v-flex mt-5 d-flex justify-center>
              <v-btn
                width="70%"
                class=""
                height="50"
                elevation="3"
                color="#f4f6fc"
                @click="dialogOn"
                >تیکت 2 تاریخ 12/12/01</v-btn
              >
            </v-flex>
            <v-flex mt-5 d-flex justify-center>
              <v-btn
                width="70%"
                class=""
                height="50"
                elevation="3"
                color="#f4f6fc"
                @click="dialogOn"
                >تیکت 3 تاریخ 12/12/01</v-btn
              >
            </v-flex>
            <v-flex mt-5 d-flex justify-center>
              <v-btn
                dark
                width="70%"
                class=""
                height="50"
                elevation="3"
                color="#5b7bb6"
                @click="dialogOn"
                >مشاهده همه</v-btn
              >
            </v-flex>
          </div>
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <v-card class="ma-5" height="370px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-face-agent</v-icon>
            ارسال تیکت
          </v-card-title>
          <v-divider inset></v-divider>
          <div class="mr-12 px-6">
            <v-flex class="mt-5">
              <v-text-field
                background-color="white"
                filled
                prefix="موضوع:"
                color="#ccdcf2"
                outlined
                hint="موضوع تیکت را وارد کنید "
                single-line
              ></v-text-field>
              <v-textarea
              background-color="white"
              outlined
               filled
                clearable
                clear-icon="mdi-close-circle"
                label="متن"
                placeholder="متن تیکت خود را تایپ کنید "
              ></v-textarea>
              
            </v-flex>
          </div>

          <v-flex class="mt-5" d-flex justify-center>
            <v-btn width="70%" class="" dark elevation="2" color="orange"
              >ویرایش</v-btn
            >
          </v-flex>
        </v-card>
      </v-col>
    </v-row>

    <!-- dialog for tiket  -->

    <v-row justify="center">
      <v-dialog v-model="dialog" width="70%">
        <v-card>
          <v-card-title>
            <span class="text-h5">تیکت شماره 123</span>
          </v-card-title>

          <v-card-text>
            موضوع : تیکت 1
            <br />
            تاریخ : 12/12/1401
            <br />
            لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با
            استفاده از طراحان گرافیک است، چاپگرها و متون بلکه روزنامه و مجله در
            ستون و سطرآنچنان که لازم است، و برای شرایط فعلی تکنولوژی مورد نیاز،
            و کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد، کتابهای
            زیادی در شصت و سه درصد گذشته حال و آینده، شناخت فراوان جامعه و
            متخصصان را می طلبد، تا با نرم افزارها شناخت بیشتری را برای طراحان
            رایانه ای علی الخصوص طراحان خلاقی، و فرهنگ پیشرو در زبان فارسی ایجاد
            کرد، در این صورت می توان امید داشت که تمام و دشواری موجود در ارائه
            راهکارها، و شرایط سخت تایپ به پایان رسد و زمان مورد نیاز شامل
            حروفچینی دستاوردهای اصلی، و جوابگوی سوالات پیوسته اهل دنیای موجود
            طراحی اساسا مورد استفاده قرار گیرد.
          </v-card-text>

          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="red darken-1" text @click="dialog = false">
              بستن
            </v-btn>
            <v-btn color="green darken-1" text @click="dialog = false">
              پاسخ
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Dashboard-Support",
  data() {
    return {
      dialog: false,
      avatarRules: [
        (value) => !value || value.size < 200000 || "کمتر از 2 مگابایت",
      ],
      nameRule: [
        (v) => !!v || " پر کردن اجباری می باشد ",
        (v) => (v && v.length >= 3) || "حداقل 3 کاراکتر",
      ],
    };
  },
  methods: {
    dialogOn() {
      this.dialog = !this.dialog;
    },
  },
};
</script>

<style scoped></style>
