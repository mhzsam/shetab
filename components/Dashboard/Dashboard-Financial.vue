<template>
  <div>
    <v-row no-gutters>
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="300px">
          <div>
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-cash-multiple</v-icon>
              اعتبار شما
            </v-card-title>
            <v-divider inset></v-divider>
            <v-flex mt-5 d-flex justify-center>
              <span class="ma-1">اعتبار شما : </span>
              <span class="ma-1"> 20000 </span>
              <span class="ma-1">ریال</span>
            </v-flex>

            <v-flex d-flex justify-center>
              <v-text-field
                class="mx-4 mt-5"
                suffix="ریال "
                background-color="white"
                filled
                prefix="مبلغ:"
                color="#ccdcf2"
                outlined
                hint="موضوع تیکت را وارد کنید "
                single-line
              ></v-text-field>

              <v-btn
                dark
                class="mx-4 mt-6"
                height="50"
                elevation="5"
                color="#5b7bb6"
                @click="dialogOn"
                >شارژ سریع</v-btn
              >
            </v-flex>
          </div>
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <v-card class="ma-5" height="300px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-credit-card-refresh</v-icon>
            خلاصه تاریخچه تراکنش
          </v-card-title>
          <v-divider inset></v-divider>
          <div class="mr-12 px-6">
            <v-flex class="mt-5">
              <v-simple-table fixed-header height="200px">
                <template v-slot:default>
                  <thead>
                    <tr>
                      <th>شماره</th>
                      <th>تاریخ</th>
                      <th>مبلغ</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="(item, index) in tabalData" :key="index">
                      <td>{{ index + 1 }}</td>
                      <td>{{ item.date }}</td>
                      <td>{{ item.price }}</td>
                    </tr>
                  </tbody>
                </template>
              </v-simple-table>
            </v-flex>
          </div>
        </v-card>
      </v-col>
    </v-row>

    <!-- dialog for tiket  -->
  </div>
</template>

<script>
export default {
  name: "Dashboard-Financial",
  data() {
    return {
      tabalData: [
        {
          date: "1400/12/12",
          price: +1000,
        },
        {
          date: "1400/12/15",
          price: "1200-",
        },
        {
          date: "1400/12/19",
          price: 5000,
        },
        {
          date: "1400/12/22",
          price: "10000-",
        },
          {
          date: "1400/12/28",
          price: 20000,
        },
      ],

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
