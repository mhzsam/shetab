<template>
  <div>
    <v-row no-gutters>
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="400px">
          <div>
            <v-card-title primary-title>
              <v-icon class="mx-4">mdi-account-circle</v-icon>
              مشخصات کاربری
            </v-card-title>
            <v-divider inset></v-divider>

            <v-flex class="mt-5 mr-5" d-flex>
              <div>
                <v-avatar max-width="180" size="80">
                  <v-img src="img/avatar/avatar.png"></v-img>
                </v-avatar>
              </div>
              <div class="m mr-5">
                <p>نام : {{ firstName }}</p>
                <p>نام خانوادگی : {{ lastName }}</p>
                <p>ایمیل : {{ email }}</p>
                <p>موجودی : {{ price }}</p>
                <p>وضعیت تیکت : تیکتی یافت نشد</p>
                <p>نوع کاربر : ویژه</p>
                <p>آخرین دوره خرید شده : دوره شماره 1</p>
              </div>
            </v-flex>
          </div>
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <v-card class="ma-5" height="400px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-battery-charging-wireless-70</v-icon>
            درصد پیشرفت
          </v-card-title>
          <v-divider inset></v-divider>
          <LinerChartPercent class="chart-responsive" />
        </v-card>
      </v-col>
      
    </v-row>
    <v-row no-gutters>
      <v-col cols="12" md="4">
        <v-card class="ma-5" height="400px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-battery-charging-wireless-70</v-icon>
          درصد پیشرفت آخرین دوره 
          </v-card-title>
          <v-divider inset></v-divider>
          <LinerChartLastCourse class="chart-responsive" />
        </v-card>
      </v-col>
      <v-col cols="12" md="8">
        <v-card class="ma-5" height="400px">
          <v-card-title primary-title>
            <v-icon class="mx-4">mdi-clock-time-eight-outline</v-icon>
       مدت زمان حضور در سایت در هفته اخیر
          </v-card-title>
          <v-divider inset></v-divider>
          <LinerChartTime class="chart-responsive" />
        </v-card>
      </v-col>
      
      
      
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Dashboard",
  data() {
    return {
      firstName: "محمد",
      lastName: "ضرابی",
      email: "mhzsam@gmail.com",
      price: 2000 + " ریال",
    };
  },
};
</script>

<style scoped>
.chart-responsive{
height: 310px !important;
margin: 10px;
}
</style>
